# XSLT Static Site Generator

## 這是什麼？

根據 [Git repository on GitHub](https://github.com/bauhouse/xslt-static-site-generator) 建立，是一個以 XML 為核心、XSLT 為模板語言與轉換工具，製作靜態 HTML 網站的生成器，與 Jekyll(Ruby)、Pico(PHP)、Assemble(Node.js) 算是同一種東西，希望能夠長大成 Static，同時也是無痛升級成動態 Symphony CMS Project 的基礎。

### 製作 HTML

XSLT 作為核心的編譯引擎（使用 Mac 與 Linux 都內建的 `xsltproc`），用來產生有效且良好（valid and well-formed）的 XHTML（更嚴謹語法的 HTML）。在 Mac 與 Linux 系統上無需安裝任何程式即可運作，視窗需自行加裝 xsltproc（未經測試）。

> To process HTML, run the `./build` script in the same directory as this README file.

> To process individual files, open the `workspace/build` file and find the xsltproc command referring to the HTML file you would like to process and run the command.

## 架構

完全自行建構。

基本上 `xsltproc -v -o 目標檔案 XSL檔案 XML檔案` 就完成了，剩餘的事務通通都在 XSL 檔案中指定（使用 utilities、取用資源、遞迴或任何進階處理）。

為了 Symphony CMS 準備專案架構，由於後續可以將所有靜態XML資源通通變成 Symphony 提供的動態資源，可以快速移轉到動態網站的實作。

除非你用 Symphony CMS，否則無需理會。