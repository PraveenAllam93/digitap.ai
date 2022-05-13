# digitap.ai

A PDF extraction from the given invoice

--> Task: Data extraction from the given PDF document of Idea Postpaid Mobile Bill Statement.

PyPDF2 is used to get the count of the number of pages in the pdf. (PyPDF2 is used to merge, transform, crop, and split the pages of PDF files).

pdfMiner.high_level is used to extract the data from a PDF file from each page. It allows you to get the exact location of the text on a page.

--> Activity #1 : Getting name, address, Mobile number, Invoice period from first page.

Using the pdfMiner.high_level extracted the data from the first page of the invoice and stored it in a list. (The type of extracted text is string).

From the extracted data, we get the required output in the JSON format.

--> Activity #2 : From the page which contains the Roaming Calls: Call Details (all details like S.No, Date, Destination, Time, Number Called, Type, Duration, and Total Amt)

Firstly, I found the roaming call details page in the pdf (after extracting the data using pdfMiner.high_level).

The extracted data is kind of mixed with two roaming call details, so I got the details for each roaming call by performing string actions.

After performing the string actions, the required output is printed in JSON format.

---> How to execute the program.

In the given .ipynb file, run each cell one after another. Give the local pdf location in the first cell as input, and run all the cells one after another until you get the required output.

Why is this specific approach used?

While researching this problem, I came up with PyPDF2 and pdfMiner. pdfMiner analyses data well and gets the exact data, so I preferred it. The extracted text is in string format, so I used string operations to get the required output.

I guess this code should work completely fine for similar Idea Postpaid Bill Mobile Statements. I have checked with sample pdf's given it works fine and gets the correct output. 

If possible, please do share the best solution for this problem.
