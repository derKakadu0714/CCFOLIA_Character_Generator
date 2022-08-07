# CCFOLIA_Character_Generator
CCFOLIA 角色生成器 使用說明
<br>
<br>
google docs 連結
https://docs.google.com/document/d/1fwtRObAQ_T238B7x3Y3PNx1M8sxSi7pvLhZlAX8s3Fs/edit?usp=sharing

# 適用範圍

**系統：** CoC

**CCFOLIA 骰子：** クトゥルフ神話TRPG

**環境：** PC only / window 10， 其他版本不確定!
[Uploading 1.png…]()


#


# 前言

雖然 CCFOLIA 近年開始受到很多玩家的喜愛及青睞，不過官方至目前為止還尚未推出帳號內儲存角色的功能，以至於每次要用既有卡片跑團時，都要重新輸入一次角色的所有狀態，尤其是每次都要重打技能指令可以說是令人非常頭痛。

但或許有很多玩家沒有注意到，CCFOLIA 其實早有推出一項「開發者面向」的，擁有角色匯入功能的 API。只不過因為是開發者面向所以並非大部分玩家能夠輕易上手使用的。

故本人以淺薄的知識寫了一個簡單的程式，讓大部分使用者能夠從此在使用CCFOLIA時輕鬆地匯入角色，再也不用每次開新團就要重新輸入數據。

詳細請見以下介紹。
CCFOLIA 角色匯入功能介紹
首先是關於官方的角色匯入功能。

簡潔扼要地說，匯入步驟為：

複製字串 → 到 CCFOLIA 的房內 → 貼上

就是這麼簡單。至於字串是什麼? 請見下圖：


這是官方文件給的資料，字串就是上圖的


{ "kind": "character", "data": { "name": "Chicken" } }


在這串文字裡儲存了角色卡的所有資料（以上文字只有角色姓名，Chicken 的資料），包括角色姓名、HP、MP、SAN 值甚至是技能指令等的數據，就只需要一個簡單的複製貼上的動作就可以輸入。


貼上的效果如下：


![2](https://user-images.githubusercontent.com/103349391/183304950-f8ebd0ef-fe18-4915-9633-f141ed9b008b.png)


![3](https://user-images.githubusercontent.com/103349391/183304978-0cbcc28e-98de-4672-87cd-1459e06089c8.png)


可以看到角色Chicken生成在面板中央


角色名稱顯示為: Chicken


因此，此工具即是能夠生成並儲存字串，將此作為角色資料以方便日後進行更改及匯入。

備註: 為何不用excel弄一張空白角卡是因為我 & 朋友們不想換角卡(



# 使用說明

**下載**

首先打開[下載連結](https://github.com/derKakadu0714/CCFOLIA_Character_Generator?fbclid=IwAR10EDbnaBu8uOYnTvtLMUTbwrmEdhtODrSu84Za0MkAxYh4tTxl2QrSCAQ)，會進到以下頁面


![image](https://user-images.githubusercontent.com/103349391/183304998-7692818e-1d1f-4d4e-8355-8997ff86a13f.png)


請點選 ![4](https://user-images.githubusercontent.com/103349391/183305104-38fbe740-5149-4207-9d4c-de18ab5e636c.png)
　＞＞　Download ZIP




下載並得到以下壓縮檔　＞＞　解壓縮

![5](https://user-images.githubusercontent.com/103349391/183305114-04d0e47b-1c16-4b90-bd3b-7fbcdade7ed1.png)


![6](https://user-images.githubusercontent.com/103349391/183305118-8418b0f6-e82d-4d79-a394-cc3e0027d922.png)


裡面的exe檔即是程式本體。


![19](https://user-images.githubusercontent.com/103349391/183305482-08da3a37-0efa-4630-a1b1-b190dd093a2a.png)


# 本體使用說明


**創立角色**


開啟本體進入介面

![7](https://user-images.githubusercontent.com/103349391/183305150-7fd79bce-2d9a-4bd6-9fa8-74d4c75bc400.png)


**步驟1 - 輸入基本資料**


在以上欄位輸入角色的基本資料，除了其他欄以外基本狀態及屬性都為必填欄位。


在此以自家小孩為例

![8](https://user-images.githubusercontent.com/103349391/183305166-26990143-5c9e-4238-80f6-a9cf32f4b14e.png)


輸入完畢後點擊下一頁，進到以下技能頁面

**步驟2 - 輸入技能**


![9](https://user-images.githubusercontent.com/103349391/183305221-fb0494e2-5890-4519-839a-40962d037a23.png)


此頁主要是用來生成技能指令用，最後的輸出形式為：


CCB<=技能數值 <顯示名稱>


實例：


![10](https://user-images.githubusercontent.com/103349391/183305252-11ab3589-3ea7-4079-bf00-2db180944c42.png)


輸入完畢後點擊「更新技能」，下列文字框會顯示新增成功的訊息。


![11](https://user-images.githubusercontent.com/103349391/183305263-bca78c74-aa8d-48cb-af7f-82b9e6072a12.png)


**步驟3 - 取得字串及存檔**


**取得字串**


點擊 取得CCFOLIA字串 按鈕後會跳出文字窗告知複製成功


![12](https://user-images.githubusercontent.com/103349391/183305276-f171ba40-6ff4-44c9-8ed6-66fb87fcdf01.png)



**存檔**


點擊 另存新檔 按鈕即可儲存為 1. txt檔案 2. json檔


![13](https://user-images.githubusercontent.com/103349391/183305299-4a4abb67-3523-46ce-9d5a-dda2d7c821b3.png)


txt檔: 將字串存入txt檔，日後要使用可以直接開起來複製文字並貼上CCFOLIA


json檔: 將字串存成json檔，主要功能用於日後修改數值，詳見更改角色數據


更改角色數據：


對於既有角色的數據更改，可使用匯入功能



**步驟1 - 於基本資料頁面匯入json檔**


![14](https://user-images.githubusercontent.com/103349391/183305315-e8d052ec-1a54-4563-8c78-0935d794aefd.png)


![15](https://user-images.githubusercontent.com/103349391/183305342-1a97150e-3e4f-42a1-8005-0f7bbbee6e94.png)


![16](https://user-images.githubusercontent.com/103349391/183305365-ea770438-630c-4b3f-8769-c0c7fd423228.png)


可以看到數據被匯入其中，進行修改後即可點擊下一頁。

![image](https://user-images.githubusercontent.com/103349391/183305396-0d5ed026-bc7c-4f56-b751-18cd477a6c54.png)



**步驟2 - 於技能頁面匯入json檔**


![18](https://user-images.githubusercontent.com/103349391/183305415-d0c5afb9-f3fd-4d86-9d79-0f9c7fa792d0.png)


此時可以新增 or 修改技能數值


**步驟3 - 存檔**


最後存為自己希望的檔案格式

# 限制
1. 一切有關圖片上傳如頭貼及差分等功能貌似暫時無法使用，故還是必須手動上傳。
 
2. 目前官方只有開啟角色匯入功能，房間內其他元件現在還無法複製

# 有生之年ㄉ展望

1. 可能想做上一頁ㄉ按鈕
