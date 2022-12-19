# Appium_config

1. make Appium configration
2. set this in terminal

` /usr/libexec/java_home --v `

copy the output and past it in the below

` export JAVA_HOME="here" `

open Android Studio and copy SDK path

` export ANDROID_HOME="/Users/{user}/Library/Android/sdk" 

`export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools`



``` java
    @BeforeClass
    public void setUp() throws MalformedURLException{
        DesiredCapabilities capabilities = new DesiredCapabilities();
        capabilities.setCapability("deviceName", "ARE-L22HN");
        capabilities.setCapability("udid", "3SKBB19513504532");
        capabilities.setCapability("platformName", "Android");
        capabilities.setCapability("platformVersion", "8.1");
        capabilities.setCapability("appPackage", "com.mcdonalds.mobileapp");
        capabilities.setCapability("appActivity", "mcdonalds.core.MainActivity");
        driver = new AndroidDriver(new URL("http://0.0.0.0:4723/wd/hub"),capabilities);
    }
```
