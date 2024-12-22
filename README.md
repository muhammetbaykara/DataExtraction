# DataExtraction

!pip install selenium

from selenium.webdriver.common.by import By 

from selenium import webdriver

from time import sleep

from selenium import webdriver

from time import sleep

chromeOptions = webdriver.ChromeOptions()

chromeOptions.add_argument("--incognito")

# chromeOptions.add_argument("--headless")  # Arka planda açık ve çalışmasını sağlıyor

driver = webdriver.Chrome(options=chromeOptions)  # options olarak düzeltildi

driver.maximize_window()        # Tam ekranda çalıştır

driver.delete_all_cookies()     # Çerezleri  Sil, Site açıldığı vakit çerezler çalışmayacak

driver.get("https://tr.tradingview.com/symbols/BTCUSD/")

driver.implicitly_wait(10)     # Site açıldığında bekleme süresi

while True:
    Fiyat_Bilgisi = driver.find_element(By.XPATH, '//*[@id="js-category-content"]/div[1]/div[1]/div/div/div/div[3]').text
    print(Fiyat_Bilgisi)
    sleep(3)


106.964USD
+891
+0,84%
Bugün itibariyle 15:40 UTC+3
106.964USD
+891
+0,84%
Bugün itibariyle 15:40 UTC+3
106.964USD
+891
+0,84%
Bugün itibariyle 15:40 UTC+3
106.972USD
+899
+0,85%
Bugün itibariyle 15:40 UTC+3
106.972USD
+899
+0,85%
Bugün itibariyle 15:40 UTC+3
106.972USD
+899
+0,85%
Bugün itibariyle 15:40 UTC+3
106.972USD
...
107.084USD
+1.011
+0,95%
Bugün itibariyle 16:02 UTC+3
Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...
Requirement already satisfied: selenium in c:\anaconda\new\lib\site-packages (4.27.1)
Requirement already satisfied: urllib3<3,>=1.26 in c:\anaconda\new\lib\site-packages (from urllib3[socks]<3,>=1.26->selenium) (2.2.3)
Requirement already satisfied: trio~=0.17 in c:\anaconda\new\lib\site-packages (from selenium) (0.27.0)
Requirement already satisfied: trio-websocket~=0.9 in c:\anaconda\new\lib\site-packages (from selenium) (0.11.1)
Requirement already satisfied: certifi>=2021.10.8 in c:\anaconda\new\lib\site-packages (from selenium) (2024.8.30)
Requirement already satisfied: typing_extensions~=4.9 in c:\anaconda\new\lib\site-packages (from selenium) (4.11.0)
Requirement already satisfied: websocket-client~=1.8 in c:\anaconda\new\lib\site-packages (from selenium) (1.8.0)
Requirement already satisfied: attrs>=23.2.0 in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (24.3.0)
Requirement already satisfied: sortedcontainers in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (2.4.0)
Requirement already satisfied: idna in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (3.7)
Requirement already satisfied: outcome in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (1.3.0.post0)
Requirement already satisfied: sniffio>=1.3.0 in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (1.3.0)
Requirement already satisfied: cffi>=1.14 in c:\anaconda\new\lib\site-packages (from trio~=0.17->selenium) (1.17.1)
Requirement already satisfied: wsproto>=0.14 in c:\anaconda\new\lib\site-packages (from trio-websocket~=0.9->selenium) (1.2.0)
Requirement already satisfied: pysocks!=1.5.7,<2.0,>=1.5.6 in c:\anaconda\new\lib\site-packages (from urllib3[socks]<3,>=1.26->selenium) (1.7.1)
Requirement already satisfied: pycparser in c:\anaconda\new\lib\site-packages (from cffi>=1.14->trio~=0.17->selenium) (2.21)
Requirement already satisfied: h11<1,>=0.9.0 in c:\anaconda\new\lib\site-packages (from wsproto>=0.14->trio-websocket~=0.9->selenium) (0.14.0)
