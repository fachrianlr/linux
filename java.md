# The driver could not establish a secure connection to SQL Server by using Secure Sockets Layer (SSL) encryption : 
locate java.security
remove TLSv1 & TLSv1.1 on file java.security
jdk.tls.disabledAlgorithms=SSLv3, TLSv1, TLSv1.1, RC4, DES, MD5withRSA, \
    DH keySize < 1024, EC keySize < 224, 3DES_EDE_CBC, anon, NULL, \
    include jdk.disabled.namedCurves

#add alternative java version jdk/open jdk in linux:
extract java folder in "/usr/lib/jvm/jdk1.8.0_271"
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_271/jre/bin/java" 1
