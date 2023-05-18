# WhiteSur firefox theme 的修復
- 針對WhiteSur的firefox theme在使用時可能會出現的問題提出的修正（雖然大部分人都可以自行解決）
- 這些代碼都不是我的，我只是做了一些小修改（來源：https://github.com/Whiteh4tWolf/WhiteSur-gtk-theme）
- 將原本的檔案取代掉，應該就可以修復下面兩個問題
# popups.css檔案(Monterey/parts/popus.css)
- 在自動填入帳密的部份，四周可能會有黑匡的出現，刪掉popus.css其中的background: var(--gnome-menu-background) !important;就可以解決問題
# left-tab-close-button.css檔案(Monterey/left-tab-close-button.css)
- 會導致頂選的tab右側也會被填充20px => 將代碼移到.tab-content:not([pinned]) 內部就可以解決問題
- 因為不明原因，釘選的tab在顯示靜音鈕的時候，會莫名變寬 => 透過限制pinned tab最大寬度的方式來修復
