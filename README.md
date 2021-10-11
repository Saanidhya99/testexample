# testexample

test to commit changes to a file
public class friday 
{
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "C:\\selenium-java-3.141.59\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.manage().deleteAllCookies();
		driver.get("https://www.amazon.in/");
		WebElement username = driver.findElement(By.id("twotabsearchtextbox"));
		Thread.sleep(1000);
		username.sendKeys("coffee");
		WebElement btn = driver.findElement(By.id("nav-search-submit-button"));
		btn.click();
		driver.findElement(By.className("s-image")).click();
		Thread.sleep(1000);
		driver.navigate().back();
		WebElement prot = driver.findElement(By.cssSelector("#twotabsearchtextbox"));
		prot.sendKeys("protein");
		WebElement btn1 = driver.findElement(By.cssSelector("#nav-search-submit-button"));
		btn1.click();
    }
