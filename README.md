# gmane
This application is an email archive analyzer that loads email messages into an SQLite database, analyzes the senders, recipients, and domains, and analyzes the data.

* **gmane.py** reads email messages from the Sakai email archive located at http://mbox.dr-chuck.net/sakai.devel/ and stores them in the content.sqlite database.

* **gmodel.py** processes and models the data from content.sqlite and stores the cleaned data in index.sqlite, which is used for the following scripts.

* **gbasic.py** prints the top email list participants, and the top organizations.

* **gword.py** finds the most common words from subject lines and writes them in JSON to gword.js, which can be viewed as a word cloud at http://htmlpreview.github.io/?https://github.com/drwaterman/gmane/blob/master/gword.htm

* **gline.py** finds the participation by each domain by month and writes it in JSON to gline.js. This is the data format that can currently be viewed as a line graph at http://htmlpreview.github.io/?https://github.com/drwaterman/gmane/blob/master/gline2.htm

* **gyear.py** finds the participation by each domain by year and writes it in JSON to gline.js
