// To convert to html file  and launch in browser:
ipython nbconvert presentation.ipynb --to slides --post serve

// To convert to static html file for running later
ipython nbconvert presentation.ipynb --to slides

// To open the html file in a browser
python -m SimpleHTTPServer 

// If the port is already in use (error: socket.error: [Errno 48] Address already in use)
ps -fA | grep python

// The second number is the process number (e.g. 501 81651 12648   0  9:53PM ttys000    0:00.16 python -m SimpleHTTPServer)
// stop the server by sending it a signal:
kill 81651

// Alternatively, run the server on a different port, by specifying the alternative port on the command line (the port number can be any number from 1024 and up, provided the port is not already taken.):
python -m SimpleHTTPServer 8910 

// then access the server at
http://localhost:8910

//RISE To initialize this nbextension in the browser every time the notebook (or other app) loads:
jupyter nbextension enable rise --py --sys-prefix
