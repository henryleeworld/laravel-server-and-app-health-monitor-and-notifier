# Laravel 10 伺服器和應用程式健康狀況監視和通知

引入 pragmarx 的 health 套件來擴增健康狀態監視功能可提供近即時的伺服器和應用程式狀態資訊，健康狀態監視功能對服務運作的各方面來說都非常重要。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移。
```sh
$ php artisan migrate
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由網頁控制面板 `/health/panel` 監視伺服器和應用程式健康情況。
- 或執行 __Artisan__ 指令的 __health:panel__ 來監視伺服器和應用程式健康情況。
```sh
$ php artisan health:panel
```

----

## 畫面截圖
![](https://i.imgur.com/kn1LMSb.png)
> 使用網頁控制面板監視伺服器和應用程式健康情況

![](https://i.imgur.com/o9zcZrc.png)
> 使用 Artisan 指令列監視伺服器和應用程式健康情況