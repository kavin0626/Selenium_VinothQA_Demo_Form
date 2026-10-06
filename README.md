# Selenium Vinoth QA Demo Form Automation

##  Project Description

This project automates the **Vinoth QA Academy Demo Form** using **Selenium WebDriver with Python**.

The program opens the demo website, enters sample information into the form, selects options from dropdowns and checkboxes, and finally submits the form automatically.

##  Technologies Used

* Python
* Selenium WebDriver
* Google Chrome
* ChromeDriver

## Website

Vinoth QA Academy Demo Site



## ⚙️ Features

* Opens Chrome browser automatically
* Navigates to the demo website
* Enters first name and last name
* Selects radio button options
* Selects checkboxes
* Enters address details
* Selects country from dropdown
* Enters date and email
* Selects time from dropdowns
* Enters phone number
* Enters comments
* Enters age
* Submits the form automatically

## 📦 Installation

Install Python and Selenium.

Install Selenium using:

```bash
pip install selenium
```


##  Code

```python
import time

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select

driver = webdriver.Chrome()
driver.get("https://vinothqaacademy.com/demo-site/")

time.sleep(15)

driver.find_element(By.ID, "vfb-5").send_keys("Kavin")
driver.find_element(By.ID, "vfb-7").send_keys("raj")

driver.find_element(By.ID, "vfb-31-1").click()

driver.find_element(By.ID, "vfb-20-0").click()
driver.find_element(By.ID, "vfb-20-4").click()

driver.find_element(By.ID, "vfb-13-address").send_keys("saveetha")
driver.find_element(By.ID, "vfb-13-address-2").send_keys("chennai Rd")
driver.find_element(By.ID, "vfb-13-zip").send_keys("chennai")

Select(
    driver.find_element(By.ID, "vfb-13-country")
).select_by_visible_text("India")

driver.find_element(By.ID, "vfb-18").send_keys("06/09/2026")
driver.find_element(By.ID, "vfb-14").send_keys("kavin12828@example.com")

Select(
    driver.find_element(By.ID, "vfb-16-hour")
).select_by_value("10")

Select(
    driver.find_element(By.ID, "vfb-16-min")
).select_by_value("30")

driver.find_element(By.ID, "vfb-19").send_keys("9942523496")
driver.find_element(By.ID, "vfb-23").send_keys(
    "This is just a sample demo"
)
driver.find_element(By.ID, "vfb-3").send_keys("33")

time.sleep(5)

driver.find_element(By.NAME, "vfb-submit").click()

time.sleep(30)
```

##  Purpose

The main purpose of this project is to practice **Selenium WebDriver automation**, including:

* Locating web elements
* Sending text to input fields
* Clicking buttons and options
* Handling dropdowns
* Automating form submission



