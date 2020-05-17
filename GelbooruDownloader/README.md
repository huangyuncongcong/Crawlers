# GelbooruDownloader

用自写轮子写的图片爬虫。

通过将图片链接保存至本地以提升速度，至于保存图片可以通过 IDM 批量下载。

缺陷是会有部分图片404，为图片后缀与原网站 URL 不同导致。

这里可行的解决方法有:

1. 先对链接发送 head 请求，判断图片是否存在，不存在就改后缀
2. 请求每个图片对应的 post，直接获取原图 URI

两种方法都挺简单，但是这也意味着会对服务器造成更大的负担。

## 更新

### 2020年5月17日 

原网站更换了 CSS 样式，导致之前的 xpath 失效，现已修复。
