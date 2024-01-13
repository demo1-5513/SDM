package basic;

import java.util.List;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

import io.github.bonigarcia.wdm.WebDriverManager;

public class TestRegistration {
	
	
  @Test
  public void launchChrome() {
	  WebDriverManager.chromedriver().setup();
	  WebDriver driver = new ChromeDriver();
	  driver.get("https://demo.automationtesting.in/Register.html");
	  
	  driver.manage().window().maximize();
	  
	  driver.findElement(By.xpath("//*[@id=\"basicBootstrapForm\"]/div[1]/div[1]/input")).sendKeys("abc");
	  driver.findElement(By.xpath("//*[@id=\"eid\"]/input")).sendKeys("my@email");
	  
	  
	  List<WebElement> radios = driver.findElements(By.name("radiooptions"));
		for (WebElement rb : radios)
		{
			if(rb.getAttribute("value").equalsIgnoreCase("Male"))
			{
				rb.click();
				break;
			}
		}
	  
		List<WebElement> chkboxes = driver.findElements(By.xpath("//*[@id=\"checkbox1\"]"));

		for (WebElement ch : chkboxes)
		{
			if(ch.getAttribute("value").equalsIgnoreCase("Cricket"))
			{
				if(!ch.isSelected())
				{
					ch.click();
					break;
				}
			}
		}
	  
	 
		 
		 driver.findElement(By.id("Button1")).click();
		   
  }
  
  
 
}
