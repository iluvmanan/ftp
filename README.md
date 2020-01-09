# ftp
ftp server

## Installation Steps

1. docker build -t iluvmanan/ftp:1.0 .

2. docker run -d -v <your-folder-path>:/home/vsftpd \\
				-p 20:20 -p 21:21 -p 47400-47470:47400-47470 \\
				-e FTP_USER=<username> \\
				-e FTP_PASS=<password> \\
				-e PASV_ADDRESS=<ip address of your server> \\
				--name ftp \\
				--restart=always iluvmanan/ftp:1.0
