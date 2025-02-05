# Movie-Data-Analysis-with-Excel
In this project, I have explored a movie dataset using various Excel functions and data analysis tools.The goal is to analyse movie profitability, Bechdel test results, and determine movie success based on specific conditions. The project involves merging data, using pivot tables, conditional formulas, and creating a dashboard for easy insights.
Key Steps

1. Merging Data using VLOOKUP

I have two sheets:

Sheet1 contains movie data with a binary value for the Bechdel test.

Sheet2 contains the actual text values for the Bechdel test results.

To merge the Bechdel test result from Sheet2 into Sheet1, I used the VLOOKUP function:

=VLOOKUP(B2,Sheet2!$B$2:$C$1777,2,FALSE)

This formula looks up the movie ID in Sheet2 and retrieves the corresponding Bechdel test result.
2. Calculating Movie Profitability

I created a new column named Profitable, which returns "Yes" if the total gross is greater than the budget and "No" otherwise.

=IF(J2>I2, "Yes", "No")

Where:

J2 represents the total gross

I2 represents the budget

Then I calculated the Total Profit by subtracting the budget from the total gross:
=J2 - I2
3. Determining Movie Success

I defined a movie as Successful if it is profitable and not made on a low budget. Otherwise, it is Unsuccessful.

=IF(AND(K2="Yes",I2<>"low"),"Successful","Unsuccessful")

Where:

K2 represents profitability (Yes/No)

I2 contains budget details

4. Creating a Dashboard

To make data retrieval easier, I created a Dashboard Sheet where users can enter a movie name and get its:

Bechdel test result

Profitability status

Using VLOOKUP, I retrieved the relevant details:
5. Adding Slicers for Interactive Filtering
To enhance data visualization and user experience, I added Slicers for:

Year
Category(Low, Medium,High)
Profitable (Yes/No)
Successful (Yes/No)
Bechdel Pass Status(Pass/Fail)
Slicers allow users to filter pivot table data interactively, making it easier to analyse trends without modifying formulas or raw data. For example, selecting a specific Year instantly updates the dashboard to show only relevant movies. Similarly, filtering by Profitable or Bechdel Pass helps in understanding patterns in movie success and inclusivity.


Conclusion

This project helps in understanding movie success factors using Excel's data analysis tools. The use of VLOOKUP, IF, AND, and pivot tables makes it easier to derive meaningful insights. The Dashboard provides a quick lookup feature for movie details, enhancing usability.

