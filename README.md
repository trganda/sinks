# Sinks

List of sink method in java.

## File Read/Write

- `java.io.FileInputStream`
- `java.nio.file.Files`
    - `newInputStream`
    - `newOutputStream`
    - `newBufferedReader`
    - `newBufferedWriter`

## Command Execution

`java.lang.Runtime`

```java
java.lang.Runtime#exec(String command)

java.lang.Runtime#exec(String command, String[] envp)

java.lang.Runtime#exec(String command, String[] envp, File dir)

java.lang.Runtime#exec(String cmdarray[])

java.lang.Runtime#exec(String[] cmdarray, String[] envp)

java.lang.Runtime#exec(String[] cmdarray, String[] envp, File dir)
```

`java.lang.ProcessBuilder`

```java
java.lang.ProcessBuilder#ProcessBuilder(List<String> command);

java.lang.ProcessBuilder#ProcessBuilder(String... command);

java.lang.ProcessBuilder#command(List<String> command);

java.lang.ProcessBuilder#command(String... command);
```

`java.lang.ProcessImpl#start`

```java
java.lang.ProcessImpl#start(String[] cmdarray, java.util.Map<String,String> environment, String dir, ProcessBuilder.Redirect[] redirects, boolean redirectErrorStream)
```

`org.springframework.context.support.ClassPathXmlApplicationContext`

```java
org.springframework.context.support.ClassPathXmlApplicationContext#ClassPathXmlApplicationContext(String configLocation)

org.springframework.context.support.ClassPathXmlApplicationContext#ClassPathXmlApplicationContext(String... configLocations)
```

`org.springframework.context.support.FileSystemXmlApplicationContext`

```java
org.springframework.context.support.FileSystemXmlApplicationContext#FileSystemXmlApplicationContext(String configLocation)

org.springframework.context.support.FileSystemXmlApplicationContext#FileSystemXmlApplicationContext(String... configLocations)
```

`java.lang.Class`

```java
java.lang.Class#forName(String className)

java.lang.Class#forNameforName(String name, boolean initialize, ClassLoader loader)

java.lang.Class#getMethod(String name, Class<?>... parameterTypes)

java.lang.Class#getDeclaredMethod(String name, Class<?>... parameterTypes)
```

`java.lang.reflect.Method`

```java
java.lang.reflect.Method#invoke(Object obj, Object... args)
```

`java.lang.reflect.Constructor`

```java
java.lang.reflect.Constructor#newInstance(Object ... initargs)
```

`java.lang.ClassLoader`

```java
java.lang.ClassLoader#loadClass(String name)

java.lang.ClassLoader#loadClass(String name, boolean resolve)

java.lang.ClassLoader#defineClass(String name, byte[] b, int off, int len)
```

`sun.reflect.misc.MethodUtil`

```java
sun.reflect.misc.MethodUtil#invoke(Method m, Object obj, Object[] params)
```

## JNDI

`javax.naming.spi.NamingManager`, `javax.naming.spi.DirectoryManager` extended the `javax.naming.spi.NamingManager`

```java
javax.naming.spi.DirectoryManager#getObjectInstance(Object refInfo, Name name, Context nameCtx, Hashtable<?,?> environment)

javax.naming.spi.NamingManager#getObjectInstance(Object refInfo, Name name, Context nameCtx, Hashtable<?,?> environment)
```

`com.sun.jndi.rmi.registry.RegistryContext`

```java
com.sun.jndi.rmi.registry.RegistryContext#lookup(Name name)

com.sun.jndi.rmi.registry.RegistryContext#lookup(String name)
```

`javax.naming.Context`

```java
javax.naming.Context#lookup(Name name)

javax.naming.Context#lookup(String name)
```

`java.rmi.registry.Registry`

```java
java.rmi.registry.Registry#lookup(String name)
```

`com.sun.jndi.url.ldap.ldapURLContext`

```java
com.sun.jndi.url.ldap.ldapURLContext#lookup(Name name)

com.sun.jndi.url.ldap.ldapURLContext#lookup(String name)
```

`org.springframework.jndi.JndiTemplate`

```java
org.springframework.jndi.JndiTemplate#lookup(String name)
```

## Server Side Request Forgery

`java.net.URL`

```java
java.net.URL#openConnection()

java.net.URL#openConnection(Proxy proxy)

java.net.URL#openStream()
```

## XML External Entity

`javax.xml.parsers.DocumentBuilder`

```java
javax.xml.parsers.DocumentBuilder#parse(File f)

javax.xml.parsers.DocumentBuilder#parse(InputStream is)

javax.xml.parsers.DocumentBuilder#parse(InputStream is, String systemId)

javax.xml.parsers.DocumentBuilder#parse(String uri)
```

`javax.xml.transform.Transformer`

```java
javax.xml.transform.Transformer#transform(Source xmlSource, Result outputTarget)
```