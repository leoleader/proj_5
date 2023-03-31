TEAM: Dylan McCann and Damian Uduevbo

Design Talk:
This program is a web crawler, which has the following plan of action when ran: it takes in the user's user name and password, optionally a server and host port, connects to the server and port, then logs into Fakebook using the provided information. It logsin by sending an HTTP get request, and then a HTTP Post request, maintainging the seesion id and cookie information. Then it travels to every profile link it finds, downloading each HTML page and parsing it to try and find secret flags. Once all 5 are found, it stops and prints the flags. The program is one main crawler class which is initialized using the command line arguments and then ran. The run method is only a few lines, calling much bigger, specialized helper methods to execute the above plan. 

Challenges:
In my opinion this project was not as challenging as some of the pasts ones (and from what I can tell the next one), using the dev tools in firefox to look at the get and post requests and structure of Fakebook made it very straightforward to understand and replicate, and the concepts behind the project were relatively easy to understand. The hardest part I would say was all the parsing that needed to be done, I actually started learning regex just so I could make the parsing easier in this project, so I would say learning and trying to implement regex with this was the most challenging part (the special characters are very confusing to me).

Strengths:
I think that the design is very clean and due to all of the functionalities necessary being split up into helper methods, it makes this complicated program easy to understand. Everything is well documented and there is little to none repetition of code and the crawler runs quickly since I integrated gzip encoding and keep-alive. 

Testing:
Throughout the design process I continuouslly ran the crawler and troubleshooted the errors we recieved, printing outputs from different parts of the program depending on what part I was analyzing/fixing. Any helper methods we made we would write some tests and run them in an outside interactive window to verify that they worked correctly independently and then would run the entire program with them to make sure they were implemented correctly. 