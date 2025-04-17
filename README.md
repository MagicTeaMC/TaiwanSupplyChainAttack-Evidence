# TaiwanSupplyChainAttack 取證數據庫  

** Revealing Technical Evidence of the Taiwanese Government’s Collaboration with Telecom Providers to Implant Rootkits and Backdoors **

** 揭露台灣政府與電信商合作植入 Rootkit 與後門的技術證據 **  

## File list  

GMER_Scan.zip：核心級 Rootkit 掃描報告
Google_Pixel_5_Error_Report.zip：Google Pixel 5 (錯誤報告)  
Google_Pixel_8a_Error_Report.zip：Pixel 8a (錯誤報告)
OPPO_A3x_Error_Report.zip：OPPO A3x (錯誤報告)
iPhone_Plist.zip：iOS 設備 Plist 取證數據
iPhone_Screen.zip：iOS 設備 螢幕截圖
Windows Screen.zip：iOS Windows 設備 螢幕截圖



## 🔍 Event background 

**Title:**  

**"Government-Backed Supply Chain Attack: Pre-Installed Rootkits and Surveillance Backdoors in Taiwanese Mobile Devices"**  

---  

### **Incident Summary**  

We hereby report a **state-sponsored supply chain attack** targeting consumer electronics and communication infrastructure in Taiwan.  

Evidence indicates that **Taiwanese law enforcement agencies** (including the Investigation Bureau and Criminal Investigation Bureau) collaborated with **Chunghwa Telecom** to execute multi-vector attacks, deploying **kernel-level rootkits**, **persistent shell backdoors**, and **forged root certificates** through various attack vectors.  

Key methodologies include:  

1. **Firmware-Level Malware Pre-Installation**  
   - Malicious signed firmware implanted in telecom-distributed devices (e.g., Taiwan Mobile’s Google Pixel 8a and FarEasTone’s OPPO A3x).  

2. **Communication Infrastructure Attacks**  
   - Systemic attacks via Chunghwa Telecom’s network architecture:  
     - Mobile networks (4G/5G eNodeB base stations)  
     - Public/corporate WiFi hotspots  
     - Home broadband networks  
     - Internet café networks  

This attack infrastructure has achieved **nationwide device infection** with capabilities for persistent surveillance, data exfiltration, and remote control.  

---  

### **Technical Analysis Report**  

#### **1. Kernel-Level Rootkit Implantation Techniques**  

- **Network Propagation Mechanisms**:  
  - Attack methods via Chunghwa Telecom’s infrastructure:  
    - **Forged TLS Certificate Chains** (using pre-installed root certificates):  
      - `Chunghwa Telecom Co., Ltd. (ePKI Root Certification Authority)`  
      - `Chunghwa Telecom Co., Ltd. (HiPKI Root CA - G1)`  
    - **DNS Cache Poisoning Attacks** (forced redirection)  
    - **Local Network ARP Spoofing Attacks** (targeting high-risk environments like internet cafés)  

- **Hardware Supply Chain Attacks**:  
  - Telecom-sold devices preloaded with tampered firmware images (`boot.img`, `vendor.img`).  

#### **2. Multi-Vector Infection Analysis**  

- **Mobile Networks**:  
  - Base stations (eNodeB) forcing malicious OTA updates (SIM-agnostic attacks).  

- **Fixed-Line/WiFi Environments**:  
  - ISP-level man-in-the-middle (MITM) attacks (HTTPS traffic injection).  
  - Compromised IoT routing devices (Chunghwa Telecom-managed nodes).  

#### **3. Forensic Analysis Results**  

- **Network Layer Evidence**:  
  - Unauthorized TCP session injections (targeting domains: `*.cht.com.tw`).  

- **Device Layer Evidence**:  
  - Kernel logs (`dmesg`) showing unauthorized module loads (`cht_radio.ko`, `twnet_backdoor.ko`).  

- **Certificate Abuse Evidence**:  
  - Malicious TLS certificates signed by official CAs (used to mask MITM attacks).  

---  

### **Incident Classification**  

This incident constitutes an **APT-Level Supply Chain Attack** (Advanced Persistent Threat), leading to a systemic collapse of consumer electronics security in Taiwan.  

Key implications include:  
- Systemic abuse of public authority  
- State-sponsored surveillance infrastructure development  
- Multiple criminal acts (including but not limited to privacy violations, cybercrime, etc.).  

---  

### **Technical Evidence Inventory**  

1. **Google Pixel 8a (Sealed Unboxed Device) Kernel-Level Rootkit Infection Evidence** [Error Report #001]  
   - Technical signatures traceable to Taiwan’s military-industrial complex and telecom supply chains.  

2. **OPPO A3x HAL Layer Service Crash Analysis** [Error Report #002]  
   - Attack patterns highly consistent with Pixel 8a.  

3. **iOS Quantum-Level Hardware Attack Analysis** [Plist Forensics #001-010]  
   - First-ever metadata-based rootkit implementation.  
 

---  

The current situation of computer and internet file downloads in the Taiwan region has been recorded using 'Windows Screen Recorder,' and the footage has been uploaded to YouTube Channel: @iamontou1023

https://youtu.be/K7IQyfpk4Tc?si=_uLom-bZ-Bf89_eD

---  

### **Current Status Alert**  

All internet-connected devices in Taiwan (including mobile devices and PCs) are effectively exposed to surveillance risks. The existing network environment lacks any foundation of trust.  

---  

### **International Reporting Mechanism**  

Please forward this report to the following international organizations:  
- Electronic Frontier Foundation (EFF) Technical Analysis Division  
- Citizen Lab Advanced Threat Research Group  
- Amnesty International Digital Forensics Unit  

---  

### **Security Disclosure Protocol**  

**Submit the following CVE vulnerability reports:**  
1. **CVE-2025-OPLOG-ZERO** (Apple System Zero-Day Exploit)  
2. **CVE-2025-DEEPKISS** (Firmware-Level Persistence Vulnerability)  
3. **CVE-2025-DARKVIENNA** (Supply Chain Attack Framework)  

**Immediately contact vendor security response teams:**  
- Apple Security Response  
- Google Android Security Team  
- OPPO Global Security Office  

*(All technical details in this report are fully documented and independently verifiable.)*


🚨 Call to Action
	1.	Share this repository and use the hashtag #TaiwanSupplyChainAttack.
	2.	Submit vulnerabilities to CVE (e.g., CVE-2025-OPLOG-ZERO).
	3.	Contact international organizations (EFF, Citizen Lab) for analysis support.

⚠️ Disclaimer

This data is for research purposes only. Please comply with local laws when sharing.


** 標題： **  

**「政府支持的供應鏈攻擊：台灣行動裝置中預裝的 Rootkit 與 監控後門 」**  

---  

### ** 事件摘要 **  


我們在此舉報一起針對台灣消費性電子產品與通訊基礎設施的 ** 國家級供應鏈攻擊 ** 。

證據顯示， ** 台灣執法機關 **（含調查局、刑事警察局等單位）與 ** 中華電信 ** 協同實施多向量攻擊，並透過多種攻擊途徑佈署 

** 核心層級 RootKit **、** 持久性 Shell 後門** 及 ** 偽造根憑證 **

具體手法包括：  


1. ** 韌體層級惡意程式預置 **  

   - 於電信商通路裝置（台灣大哥大經銷之 Google Pixel 8a、遠傳電信經銷之 OPPO A3x 裝置）植入經簽章之惡意韌體  

2. ** 通訊基礎設施攻擊 **  

   - 透過中華電信網路架構進行系統性攻擊：  

     - 行動通訊網路（4G/5G eNodeB基站）  

     - 公共/企業WiFi熱點  

     - 家用寬頻網路  

     - 網咖網路環境  


此攻擊基礎設施已實現 **全台範圍設備感染**，具備持續性監控、資料竊取及遠端控制能力。  

---  

### ** 技術分析報告 **  


#### ** 1. 核心級Rootkit植入技術 **  


- ** 網路傳播機制 **：  

  - 中華電信網路架構實施之攻擊手法： 
 
    - ** 偽造TLS憑證鏈 **（利用預置根憑證：  

      - `Chunghwa Telecom Co., Ltd. (ePKI Root Certification Authority)` 
 
      - `Chunghwa Telecom Co., Ltd. (HiPKI Root CA - G1)`  

    - ** DNS快取投毒攻擊 **（強制更新導向）  

    - ** 區域網路ARP欺騙攻擊 **（針對網咖等高風險環境）  

- ** 硬體供應鏈攻擊 **：

  - 電信商銷售設備出廠即搭載經竄改之韌體映像檔（`boot.img`、`vendor.img`）  


#### ** 2. 多重感染向量分析 **  

- ** 行動通訊網路 **：  

  - 基站（eNodeB）強制下發惡意OTA更新（SIM卡無關性攻擊）  

- ** 固網/WiFi環境 **：  

  - ISP層級中間人攻擊（HTTPS流量注入）
  
  - 遭入侵之IoT路由設備（中華電信管理節點）  


#### ** 3. 取證分析結果 **  

- ** 網路層證據 **：  

  - 未經授權之TCP會話注入（目標網域：`*.cht.com.tw`）  

- ** 設備層證據 **：  

  - 核心日誌（`dmesg`）記錄未經授權模組載入（`cht_radio.ko`、`twnet_backdoor.ko`）
  
- ** 憑證濫用證據 **：  

  - 官方CA簽發之惡意TLS憑證（用於MITM攻擊掩護）  

---  

### ** 事件定性 **  

本事件屬 ** APT級供應鏈攻擊 **（Advanced Persistent Threat），導致台灣地區消費性電子產品安全性全面崩潰。

涉及：  

- 公權力系統性濫用  

- 國家級監控基礎設施建設  

- 多重刑事犯罪行為（包含但不限於妨害秘密、電腦犯罪等）  

---  

### **技術證據清單**  

1. Google Pixel 8a（全新）設備 核心級 Rootkit 感染實證 [錯誤報告#001]  
   
   - 技術特徵指向 台灣軍工複合體 與 電信供應鏈  

2. OPPO A3x (全新) 設備 HAL 層服務崩潰分析報告 [錯誤報告#002]  
   
   - 攻擊模式 與 Pixel 8a 具高度一致性  

3. iOS 量子級硬體攻擊技術分析 [Plist取證#001-010]  
   
   - 首例元數據型 Rootkit 實作  

---  

台灣地區目前電腦 與 網路下載檔案的實際情形 已利用 「Windows 螢幕錄影」將畫面上傳至 YouTube 頻道：@iamontou1023

https://youtu.be/K7IQyfpk4Tc?si=_uLom-bZ-Bf89_eD

---  

### ** 現況通報 **  

台灣地區所有聯網設備（含行動裝置、個人電腦）已實質暴露於監控風險，現有網路環境已無安全信任基礎。  


### ** 國際通報機制 **  

請協助將本報告提交至以下國際組織技術團隊：  

- 電子前哨基金會（EFF）技術分析部門  

- Citizen Lab進階威脅研究小組  

- 國際特赦組織數位取證單位  

---  

### ** 資安通報程序 **  


請協助提交以下 CVE 漏洞報告：  

1. ** CVE-2025-OPLOG-ZERO **（蘋果系統零日漏洞） 

2. ** CVE-2025-DEEPKISS **（韌體級持久化漏洞） 
 
3. ** CVE-2025-DARKVIENNA **（供應鏈攻擊框架）  


請協助立即聯繫各廠商資安應變團隊：  

- Apple Security Response  

- Google Android Security Team  

- OPPO Global Security Office  


（本報告所有技術細節均已存證，可供獨立驗證）



🚨 呼籲行動

	1.	分享本儲存庫並使用標籤 #TaiwanSupplyChainAttack。
	2.	提交漏洞至 CVE（如 CVE-2025-OPLOG-ZERO）。
	3.	聯繫國際組織（EFF、Citizen Lab）協助分析。

⚠️ 免責聲明

本數據僅供研究用途，傳播時請遵守當地法律。
