<Installation of MYSQL>
 - Download : https://dev.mysql.com/downloads/installer/  (Reference: https://all-record.tistory.com/93)
 - Setting the Environment Variable
    : Add the the path of installation(C:\Program Files\MySQL\MySQL Server 8.0\bin) in the system variable.

 (@: There is no password field after mysql 5.7! Instead, the authentication string field replaces the password field.
        So, you can solve this problem by writing under the code.
         -> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

----------------------------------------------------------------------------------------------------------------------
<Installation of Node.js>
 - Download : https://nodejs.org/ko/
  (Considering stability and compatibility, the latest version is not recommended...)

----------------------------------------------------------------------------------------------------------------------
<Explanation of Total Code>
 1. Structure of Server
   - server.js                (Server file to run)
   - Database
     - node2db.js             (Package of functions for interworking MySQL)
     - weather.xml            (xml file of rss data in the Meteorological Administration)
     - xml2db.js              (Convert xml to JSON, parsing data, using MySQL)
   - Handling
     - socket_io.js           (Communication using socket for load the data list)
   - sslCertificate           (ssl key for use a https protocol)
     - certificate.pem
     - certrequest.csr
     - privatekey.pem
   - Client
     - assets                 (Picture and favicon)
     - bootstrap              (For use the List templete more easily)
     - css                    (Style frame about pages)
     - javascript
       - main.41beeca9.js     (Frame about 'index.html')
       - monitoring.js        (main function for 'monitoring.js')
     - jquery                 (package for using Jquery)
     - socket.io-client       (package for using socket.io communication)
     - index.html             (Main Introduction)
     - monitoring.html        (Load the weather information to real-time)
     - contact.html           ()
     - about.html             ()

  (Refered by remark every code file