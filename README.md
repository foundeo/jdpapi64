# jdpapi64

This is simply a 64 bit version / dll of [jdpapi project on sourceforge](http://jdpapi.sourceforge.net/)

## What is JDPAPI

JDPAPI is a Java Native Interface (JNI) wrapper allowing you to use the Microsoft Data Protection API (MS DPAPI) from Java.

## What is DPAPI

Microsoft Data Protection API (MS DPAPI) is an operating system level API that provides data encryption services. The OS handles the encryption key storage and protection. You can encrypt and decrypt data using a key global to the server or the user.

## How do you use JDPAPI in Java

In order to use it, you must have the `jdpapi64.dll` in your system path (find in the lib folder of this project). You can do this at runtime by invoking `System.load("c:\path\to\jdpapi64.dll")`

You must also have the jdpapi jar file in your java classpath (find in the lib folder of this project).

```java
net.sourceforge.jdpapi.DataProtector dpapi = new net.sourceforge.jdpapi.DataProtector();
byte[] encryptedData = dpapi.protect("testing");
//...
String decrypted = dpapi.unprotect(encryptedData);
System.out.println(decrypted);
```

See the [javadocs](http://jdpapi.sourceforge.net/jdpapi-java/apidocs/index.html) for more info.
