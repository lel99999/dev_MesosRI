# dev_MesosRI
Mesos re-implementation/Re-imagined/Reference Implementation

#### Docker Containerization
- [http://mesos.apache.org/documentation/latest/docker-containerizer/](http://mesos.apache.org/documentation/latest/docker-containerizer/) <br/>
 
#### Update

#### Log4j Fix for v1.2.x & v2.x
- v1.2 <br/>
  Class File	           CVE <br/>
  org/apache/log4j/net/SocketAppender.class	CVE-2019-17571 <br/>
  org/apache/log4j/net/SocketServer.class	CVE-2019-17571   <br/>
  org/apache/log4j/net/SMTPAppender$1.class	CVE-2020-9488  <br/>
  org/apache/log4j/net/SMTPAppender.class	CVE-2020-9488    <br/>
  org/apache/log4j/net/JMSAppender.class	CVE-2021-4104     <br/>
  org/apache/log4j/net/JDBCAppender.class	CVE-2022-23305   <br/>
  org/apache/log4j/chainsaw/*.class	CVE-2022-23307         <br/>
  
  ```
  ## Remove Class file
  $sudo zip -d log4j-1.2.17.jar 'org/apache/log4j/net/JMSAppender.class'
  
  ## Remove Multiple Class files
  $sudo zip -d log4j.jar 'org/apache/log4j/net/JMSAppender.class' 'org/apache/log4j/net/SocketAppender.class' 'org/apache/log4j/net/SocketServer.class' 'org/apache/log4j/net/SMTPAppender$1.class' 'org/apache/log4j/net/SMTPAppender.class'
  ```
  
- v2.x <br/>
  ```
  $sudo zip -q -d "$LOG4J_JAR" org/apache/logging/log4j/core/lookup/JndiLookup.class
  ```
