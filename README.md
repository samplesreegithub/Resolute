# Resolute
package assign;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.devtools.v102.browser.Browser;
import org.openqa.selenium.interactions.Actions;

import io.github.bonigarcia.wdm.WebDriverManager;

public class Resolute {



	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver","C:\\Selenium\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("https://facegenie-ams-school.web.app/");
		driver.manage().window().maximize();
		driver.findElement(By.id("mail id")).sendKeys("testbams@gmail.com");
		driver.findElement(By.id("user_password")).sendKeys("facegenie");
		driver.findElement(By.id("login button")).click();
		System.out.println("login successfully");
		Thread.sleep(5);
		
		
		driver.findElement(By.xpath("//h1[contains(text(), 'Dashboard')]"));
		driver.findElement(By.id("calendar"));
		driver.findElement(By.id("select bus-dropdown"));
		driver.findElement(By.id("total activities"));
		driver.findElement(By.id("total students"));
		driver.findElement(By.id("students chekedin"));
		driver.findElement(By.xpath("//h2[contains(text(), 'Attendance Logs')]"));
		driver.findElement(By.xpath("//h3[contains(text(), 'Analytics and Reports')]"));
		driver.findElement(By.linkText("Log Out")).click();
		Actions act = new Actions(driver);
		System.out.println("logout is successful");
				

	}

}
