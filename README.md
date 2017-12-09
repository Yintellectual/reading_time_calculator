User Requires:

Reading can and should be arranged. Predicate the time of reading a certain article allows the reader to make economic judgement, to slot the time, and to make a plan for it. However, making an exact predication comes with a price that can be so high that overweights the benefits. This software is going to make the predication easier by calculating the time automatically and remembering key configurations like reading speed of the user and word per line/page of the book. 

User stories:

Story 1. Show me how many minutes to read this part.
Peter easily know the number of lines/pages from counting. He opens the website and enters the number. He clicks "calculate", and get an immediate result of how many minutes for him to read. 

Task 1.1 make a new spring boot project, with web support. 
Task 1.2 set default wpm = 20 and wpl = 40. create a service called "ReadingTimeCalculator" with method calculate(lines). 
      the math is: ( lines * wpl )/wpm = minutes
      all numbers involved are integers. wpm>0, wpl>0, lines>0.
      tests:
      lines = 20, minutes = 40
      lines = 80, minutes = 160
Task 1.3 form a web ui that allows number input, submit, and display without having to refresh the page
Task 1.4 create a controller that takes in the input, call the service and send the UI output

Story 2. Configure some numbers
Peter found the default constants are not right for him or his book. So, he enter the correct constants in the configuration area, click "save". The constants are saved somewhere safe from redis reset or software restart. 

Story 3. I have to shift among many books
Peter choose the current book from a select list, click "confirm". 

Story 4. I got a new book
Peter clicks "add book", and enter a page for adding new books. He enters the book name, comments, words per line/page, click "save". The storage should be safe somewhere as a file. 

Story 5. I want to play with books
Peter got crazy and want to delete and modify the book name. He should be satisfied. The "add book" page has a select list of books. Peter select one book to "load", edit it, and "save" or "delete". 
