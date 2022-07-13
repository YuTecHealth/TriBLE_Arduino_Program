# 開發者如何在Arduino上開發TriBLE？

#### **1. 了解 TriBLE 母板的基本資訊**

* __a. 腳位格局__ <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/Pin_config.png" align="middle"
  alt="Yutech logo" width="600" height=""></code>
* __b. 腳位功能__ <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/Pin_func.png" align="middle"
  alt="Yutech logo" width="500" height=""></code>

#### **2. 在 Arduino IDE 上開發 TriBLE**
* ___a. 環境建置___: 透過「開發板管理員」安裝 Yutech nRF52 Board 的開發板
	* I. [下載並安裝Arduino IDE程式](https://www.arduino.cc/en/Main/Software) (至少要 v1.6.12)
		* 選擇你的作業程式。
		* 在頁面上直接點擊 **'Just Download'** 。 <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_1.png" align="middle"
     alt="Yutech logo" width="300" height=""></code>
	* II. 開啟 Arduino IDE 程式 (如果是 linux 使用者, 請使用 **sudo su** 方式打開 Arduino IDE程式
	* III. 在Arduino IDE選單上，點選 偏好設定
	* IV. 在「額外的開發板管理網址」欄位貼上 `https://raw.githubusercontent.com/YuTecHealth/silver-bassoon/master/package_Yutech_index.json`  <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_2.png" align="middle"
     alt="Yutech logo" width="600" height=""></code>
	* V. 關閉程式並重新開啟 Arduino IDE (如果是 linux 使用者, 請輸入下列指令 `sudo pip3 install adafruit-nrfutil` 或是 `sudo pip install adafruit-nrfutil`，再開啟Arduino IDE程式。)
	* VI. 點選 `工具 > 開發板 > 開發板管理員 ` 來開啟開發板管理員介面
		* 輸入 "Yutech" 找到 **"Yutech nRF52 by Yutech"** 並安裝最新版本。 <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_3.png" align="middle"
     alt="Yutech logo" width="600" height=""></code>
	* VII. 安裝成功後，點選 `工具 > 開發板 > Yutech TriAnswer Boards (nRF52 Series) ` 找到這個 Yutech 開發板即完成環境建置。 <br>  <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_4.png" align="middle"
     alt="Yutech logo" width="600" height=""></code>
	* **(附錄一)** 如何更改語言.
			* 檔案 -> 偏好設定 -> 編輯器語言 <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_5.png" align="middle"
     alt="Yutech logo" width="500" height=""></code>
	*  **(附錄二)** Window 7 的電腦需要額外安裝驅動程式
		*  win 7 的 Yutech 驅動程式 [點此下載](https://github.com/YuTecHealth/BoardDriver/blob/master/YuTech_drivers_0.0.0.2.exe?raw=true)
		*  [更多有關此驅動程式的資訊](https://github.com/YuTecHealth/BoardDriver)
  
* __b. **上傳** 你的程式碼__
	* I. 使用官方範例程式，或修改完你的程式碼。
	* II. 將 **TriBLE裝置** 與電腦連接 (以USB供電模式)
	* III. 在Arduino IDE選單上，點選 `工具 > 開發板 > Yutech TriAnswer Boards (nRF52 Series) > Yutech TriBLE nRF52840` <br>  <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_4.png" align="middle"
 alt="Yutech logo" width="600" height=""></code>
	* IV. 點選 `工具 > 序列埠 > COMXX (Yutech TriBLE nRF52840)` <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_18.png" align="middle"
 alt="Yutech logo" width="500" height=""></code>
	* V. 點擊 <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_upload.png" align="middle"
alt="Yutech logo" height="18" height=""></code> (編譯 + 上傳), 或 點擊 <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_V.png" align="middle"
alt="Yutech logo" height="18" height=""></code> (編譯), 成功後點擊 <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_upload.png" align="middle"
alt="Yutech logo" height="18" height=""></code> (上傳)).
	* **上傳成功 👋 會看到如下圖 "Device programmed"** <br>  <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/readme_22.png" align="middle"
    alt="Yutech logo" width="700" height=""></code>
    
#### **C. TriBLE 範例程式 與 實驗學習**    
*  __a. 如何開始:__ [**依前面步驟**](https://github.com/YuTecHealth/TriBLE_Arduino_Program/blob/main/README.md#2-%E5%9C%A8-arduino-ide-%E4%B8%8A%E9%96%8B%E7%99%BC-trible)完成Yutech環境建置後，點選 `檔案 > 範例 > YuTech TriBLE nRF52840`，選擇一個Lab進行實驗學習。 <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/arduino_example.png" align="middle"
    alt="Yutech logo" width="700" height=""></code>
*  __b. 軟體介面呈現:__ 
	* Android 介面  [**點此**](https://github.com/YuTecHealth/TriAnswer-SCR-APP/raw/main/TriAnswer_SCR_newVer_2022.apk) <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/Android_SCR1.jpg" align="middle" 
    alt="Yutech logo" width="300" height=""></code> <br>
	* 網頁介面  [**點此**](https://yutechealth.github.io/PWA/LAB5/LAB5.html) <br> <code><img src="https://github.com/YuTecHealth/YuTecHealth/blob/master/Asset/TriBLE_nRF52_Arduino/PWA1.png" align="middle"
    alt="Yutech logo" width="700" height=""></code>


#### **D. 更多韌體開發說明，請參考YuTech TriAnswer韌體主頁**   [**點此**](https://github.com/YuTecHealth/TriBLE_nRF52_Arduino)
