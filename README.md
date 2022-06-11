Calculator.js: a node.js Demonstration Project
==============================================
An example node.js project, including tests with mocha, that behaves like
a pocket calculator.

[![Build Status](https://dev.azure.com/pkhieu1989/Integrating%20External%20Source%20Control%20with%20Azure%20Pipelines/_apis/build/status/pkhieu.calculator?branchName=master)](https://dev.azure.com/pkhieu1989/Integrating%20External%20Source%20Control%20with%20Azure%20Pipelines/_build/latest?definitionId=11&branchName=master)

The project contains a simple node.js application that exposes REST APIs
to perform arithmetic on integers, and provides a test suite with mocha
and chai.  The `mocha-junit-reporters` package is included to provide XML
output that can be presented in a continuous integration tool like
[Azure DevOps](https://azure.com/devops).

To build, simply:

1. Runs `npm install` to install dependencies.
2. Runs `npm test` to run Mocha and execute the unit tests.

[https://github.com/SeleniumHQ/selenium/releases/download/selenium-3.13.0/selenium-server-standalone-3.13.0.jar ](https://chromedriver.storage.googleapis.com/index.html?path=90.0.4430.24/ )

package test;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class first {
	public static void main(String[] args) throws InterruptedException{
		System.setProperty("webdriver.chrome.driver", "/Path_To_Your_Chrome_Driver");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.manage().deleteAllCookies();
		driver.manage().timeouts().pageLoadTimeout(40, TimeUnit.SECONDS);
		driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
		driver.get("https://login.yahoo.com");
		driver.findElement(By.xpath("//input[@id='login-username']")).sendKeys("xyzz@yahoo.com");
	}	
}
