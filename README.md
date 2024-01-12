# TerriblePortScaner
First port scanner I made just to try out my skills, its pretty crappy but it does work
Included some minor error handling as well
- It takes a command-line argument, expecting the user to provide the target IP address or hostname.
- If the user provides the correct number of arguments (2), it translates the hostname to its corresponding IPv4 address using socket.gethostbyname.
- It prints a banner indicating the target being scanned and the current time.
- It then attempts to connect to a range of ports (from 50 to 85) on the specified target using a for loop.
- For each port, it creates a socket, sets a timeout of 1 second, and attempts to establish a connection (socket.SOCK_STREAM) to the target port.
- If the connection attempt (connect_ex) is successful (result equals 0), it prints a message indicating that the port is open.
- The program handles exceptions such as a KeyboardInterrupt (Ctrl+C) by printing a message and exiting gracefully.
- Other exceptions, such as a failure to resolve the hostname or connect to the server, are caught with appropriate error messages.
