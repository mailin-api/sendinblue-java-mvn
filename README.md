# SendinBlue Mvn Central Repository

> **Note:** The latest **API V3.0** ( LTS ) is now maintained at <code>https://github.com/sendinblue/</code> and the Documentation is available here <code>https://developers.sendinblue.com</code>

This is [SendinBlue](https://www.sendinblue.com) provided API V2 Mvn central repository. It implements the various exposed APIs that you can read more about on https://apidocs.sendinblue.com.

SendinBlue API's use HTTP Authentication through an api key. You can create your api key from [API Console](https://my.sendinblue.com/advanced/apikey), after you sign up for an account with SendinBlue. You must use latest version 2.0, access key, for accessing APIs.


## Install Package

The following recommended installation steps. If you are unfamiliar with maven central repository, see the [About Maven Central Repository](https://www.tutorialspoint.com/maven/maven_repositories.htm).

Our maven package is available [here](http://search.maven.org/#search|ga|1|g:"com.sendinblue")

Add the following to your `pom.xml` file:

```xml
{
  ...
  <dependencies>
      <dependency>
         <groupId>com.sendinblue</groupId>
         <artifactId>sendinblue</artifactId>
         <version>2.0</version>
      </dependency>
   <dependencies>
   ...
}
```

### Alternative installation
To download the jar pacakage [click here](http://search.maven.org/#search|ga|1|g:"com.sendinblue")


## Usage

Assuming that you have download jar file from above mention URL. You will get a jar file named sendinblue-2.0.

* Create a file MyClass.java using below code :-

```java
import com.sendinblue.Sendinblue;
import java.util.*;

class MyClass
{
    public static void main(String[] args)
    {
    	Sendinblue http = new Sendinblue("https://api.sendinblue.com/v2.0","your_api_key");
	    String accountDetail = http.get_account();
	    System.out.println(accountDetail);
	    System.out.println(" ");

	    String smtpDetail = http.get_smtp_details();
	    System.out.println(smtpDetail);
	    System.out.println(" ");
    }
}
```

* Compile and execute above java file with Sendinblue API package

```bash 
javac -cp '.:sendinblue-2.0.jar' MyClass.java
java -cp '.:sendinblue-2.0.jar' MyClass
```

## Support and Feedback

Be sure to visit the SendinBlue official [documentation website](https://apidocs.sendinblue.com) for additional information about our API.

If you find a bug, please submit the issue in [Github directly](https://github.com/mailin-api/sendinblue-java-mvn/issues). 

As always, if you need additional assistance, drop us a note [here](https://apidocs.sendinblue.com/support/).
