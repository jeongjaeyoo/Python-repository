from selenium import webdriver 
import time 

driver = webdriver.Chrome('./chromedriver')

#기숙사 로그인 페이지 접속
login_url = 'https://dorm.pusan.ac.kr/login?type=dorm'
driver.get(login_url)

time.sleep(2)

my_id ='201742151'
my_pw = 'wjdrud477!'

driver.execute_script("document.getElementsByName('userId')[0].value = \'" + my_id + "\'")
driver.execute_script("document.getElementsByName('userPw')[0].value = \'" + my_pw + "\'")

time.sleep(1)

button = driver.find_element_by_css_selector('button.btn_login')
button.click()

time.sleep(4)

menu = driver.find_element_by_xpath('/html/body/header/div/div/div[1]/ul/li[2]/a/span')
menu.click()

time.sleep(5)

dic = {}
a= []

informations = driver.find_elements_by_class_name('col-sm-2.col-xs-4.bg_lightgrey.text-center')
for information in informations:
    a.append(information.text)

details = driver.find_elements_by_css_selector('td.col-sm-10.col-xs-8')

number = 0
for word in details:
    dic[a[number]]=word.text
    number += 1

print(dic)
