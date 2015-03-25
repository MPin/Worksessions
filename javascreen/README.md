Java Screen:

The purpose of the Java screen is to serve as a stepping stone interface between clients and the database. All clients will connect to the Java screen via a socket. The Java interface will handle ping requests from client's machine by analysing which specific subset of data to grab from the database. In addition, we are currently planning to use FirebaseIO as our way to quickly organize and collect data. At some point in the future, I would like to implement a local SQL DB. Using a Java screen leaves our middle end (not front, not back) operational while we work on a backend. 

Current structure:

I would like to use sockets containing JSON information to quickly transmit relevant data. The ping data structure should have a Location (Longitude and latitude), interests (An array of tags which the user would be interested in), possibly a timeframe, a boolean 'ping all' category (downloads all data pins), and finally search criterion (ie tech, finance, party, etc).

The java structure will, in return, send a module/pin object depending on which events it wants to update and maybe some other metadata. 

There will also be another socket packet to handle user action like commenting, voting, submitting a pin, etc.

