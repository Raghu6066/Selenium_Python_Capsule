Day 1: Introduction to Selenium & Setup

✅ What is Selenium?

Selenium is a popular open-source automation tool used to automate web browsers. It supports multiple programming languages, and we will be focusing on Python.

✅ Components of Selenium:

Selenium WebDriver

Selenium IDE

Selenium Grid

✅ Installing Selenium for Python:

pip install selenium

✅ Selenium 3 vs Selenium 4 - Key Differences:

Feature                Selenium 3                                           Selenium 4

Architecture        Requires JSON Wire Protocol                             Requires JSON Wire Protocol

Uses                W3C WebDriver                                           protocol directly

WebDriver setup     Needs DesiredCapabilities                               Uses Options class

Browser-specific    driver classes Direct instantiation (e.g. Chrome())     Improved and unified handling

Relative Locators   Not supported                                           Introduced

DevTools Protocol Support   Not supported                                   Supported


Example Selenium 4 Setup:

from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager

options = webdriver.ChromeOptions()
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install()), options=options)
driver.get("https://www.google.com")

✅ Setting up WebDriver:

Download ChromeDriver

Add it to your system PATH

from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://www.google.com")

✅ Selenium IDE:

Install from Chrome/Firefox Web Store

Record, playback, and export test scripts

Limited to basic testing; for advanced use cases, prefer WebDriver