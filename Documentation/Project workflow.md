## Step-by-step Project workflow:

1. We created a mockup to understand our requirements from the dashboard.
   
<img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Mockup.png" class="center">

2. we uploaded the file in Power BI and transformed the data in power query. we change all moths in one column using the un-pivot option. we also change the Data column type to Date and added one column year(type text), then closed and applied.


<img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">

3. In Power BI, we created some measures and started building KPIs. 

       Values = sum(FinData[Value])
       Total incomes = CALCULATE(sum(FinData[Value]),FinData[Type]="Income")
       Total Expense = CALCULATE(sum(FinData[Value]),FinData[Type]="Expense")
       Total savings = CALCULATE(sum(FinData[Value]),FinData[Type]="savings")
       Title = "Finance dashboard"
       savings % = DIVIDE([Total savings],[Total incomes],0)
       Expense % = DIVIDE([Total Expense],[Total incomes],0)

4. We created These four KPIs: INCOME, Expense %, Savings%, and savings in two sets. One set is filtered by date and year but the other remains the same by edit interactions.

   <img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/KPIs.png" class="center">


5. After this, we created two clustered bar charts: components vs. total expense(in %) and components vs. total savings(in %) resp.

   <img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Clustered%20bar%20chart.png" class="center">


6. We again created some measures.

       Income LM = CALCULATE([Total incomes],DATEADD(FinData[Date],-1, MONTH))
       Income change MoM % = divide([Total incomes],[Income LM])
       saving Target % = 0.25  ---- Imaginary thing

       
7. We created one line chart: Date vs. income change MoM%, expense%, saving target %, savings %.

    <img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/line%20chart.png" class="center">


8. we created a detailed statement using the matrix: (type, components)column Vs. (Year, Date)rows Vs. (Values) values.

    <img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">

   
9. we also created four tooltips:

   <img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">
<img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">
<img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">
<img src="https://github.com/prashantsingh8962/Personal_Finance_Analysis/blob/main/Resources/Power_query.png" class="center">

