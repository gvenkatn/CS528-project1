# Binghamton University, Fall 2023

## CS428/528 Project-1: Web Server

### SUMMARY

+ There are 2 programs 
    + PART 1 - webserver1.cpp is a Single-threaded web server written in C++.
    + PART 3 - webserver2.cpp is a Multi-threaded web server written in C++. 
+ The server listens on a specified port 52837, accepts incoming client connections, and serves HTML and PDF files to clients. 
+ Each client connection is handled in a separate thread in the webserver3.cpp program, allowing the server to handle multiple client requests concurrently. 
+ The server parses incoming HTTP requests, retrieves requested files, and sends HTTP responses, supporting basic web server functionalities.
+ The server supports only "GET" request method and HTML and PDF file type. 

### NOTES, KNOWN BUGS, AND/OR INCOMPLETE PARTS

+ The servers were tested and handles upto 500MB PDF File transfers.
+ The service was denied on repeated request to the server for large PDF Files (500MB).
+ Multithreading is implemented with pthread to support all versions of C++. "thread" is compatible only after C++ 11
+ The servers were tested with 10MB, 50MB, 100MB and 500MB PDF File size.
+ The servers were tested through client requests in the same network.
+ If the client denies the response (cancels PDF download) the server raises error and is terminated.
+ Can switch to "DEBUG" mode to analyse the program flow. (to switch set const bool DEBUG = true;)

### REFERENCES

+ [Client-Server chat in C++ using sockets by KARIM OUMGHAR](https://simpledevcode.wordpress.com/2016/06/16/client-server-chat-in-c-using-sockets/)
+ [TCP File Transfer](https://github.com/Wizardous/TCP-File-Transfer/blob/dbd80ba734c65efdb0f7b19c506ca8a7c640f223/file_server.cpp#L79)
+ [GeeksForGeeks Socket Programming](https://geeksforgeeks.org/socket-programming-cc/#)
+ [POSIX thread](https://www.cs.cmu.edu/afs/cs/academic/class/15492-f07/www/pthreads.html#:~:text=POSIX%20thread%20(pthread)%20libraries,a%20new%20concurrent%20process%20flow.)
+ [Pros and Cons of pthreads versus C11 threads](https://gustedt.wordpress.com/2012/10/14/c11-defects-c-threads-are-not-realizable-with-posix-threads/)
+ [Multithreading Best Practices](https://www.developer.com/java/java-multithreading-best-practices/#:~:text=Use%20Thread%20Pools&text=Thread%20pools%20can%20help%20to,you%20need%20to%20execute%20something.)
+ [convert values between host and network byte order](https://manpages.ubuntu.com/manpages/xenial/man3/byteorder.3.html#:~:text=The%20htonl()%20function%20converts,order%20to%20network%20byte%20order.)
+ [10,50,100 MB PDF Test Files](https://testfile.org/all-pdf-sample-test-file-download-direct/)
+ [500 MB PDF Test File](https://www.learningcontainer.com/sample-pdf-files-for-testing/#)

### INSTRUCTIONS

+ Download the folder
+ Open command line/ terminal.
+ To run Single threaded web server
    + Execute the below commands        
    +       g++ webserver1.cpp -o server 
           ./server
    + OR
    +       g++ webserver1.cpp -o server; ./server
+ Request the following files using the URLs through a browser(client)
    + http://127.0.0.1:52837/home.html
    + http://127.0.0.1:52837/project1-webserver.pdf
    + http://127.0.0.1:52837/10mb.pdf
    + http://127.0.0.1:52837/50mb.pdf
    + http://127.0.0.1:52837/100mb.pdf
    + http://127.0.0.1:52837/500mb.pdf
    + ctrl+c to stop the server
+ To run Multi-threaded web server
    + Execute the below commands
    +       g++ webserver2.cpp -o server 
           ./server
    + OR
    +       g++ webserver2.cpp -o server; ./server
+ Request the following files using the URLs through a browser(client)
    + http://127.0.0.1:52837/home.html
    + http://127.0.0.1:52837/project1-webserver.pdf
    + http://127.0.0.1:52837/10mb.pdf
    + http://127.0.0.1:52837/50mb.pdf
    + http://127.0.0.1:52837/100mb.pdf
    + http://127.0.0.1:52837/500mb.pdf
    + ctrl+c to stop the server

### SUBMISSION

I have done this assignment completely on my own. I have not copied it, nor have I given my solution to anyone else. I understand that if I am involved in plagiarism or cheating I will have to sign an official form that I have cheated and that this form will be stored in my official university record. I also understand that I will receive a grade of "0" for the involved assignment and my grade will be reduced by one level (e.g., from "A" to "A-" or from "B+" to "B") for my first offense, and that I will receive a grade of "F" for the course for any additional offense of any kind.

By signing my name below and submitting the project, I confirm the above statement is true and that I have followed the course guidelines and policies.

Submission date: 11 OCTOBER 2023

Team member 1 name: VENKATNARAYAN GNANAGURUPARAN

Team member 2 name (N/A, if not applicable): Sowmya Achu

