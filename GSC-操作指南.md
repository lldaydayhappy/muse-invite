# Muse 邀请码落地页 — Google 收录操作指南

页面：https://lldaydayhappy.github.io/muse-invite/
仓库：https://github.com/lldaydayhappy/muse-invite

## 已完成（无需你操作）

- [x] GitHub Pages 已启用并上线（HTTPS，强制）
- [x] sitemap.xml 已部署并可访问
- [x] robots.txt 已部署（允许全站抓取）
- [x] canonical 标签已设置
- [x] OG 标签已设置（分享到微信/微博时显示标题和描述）
- [x] Bing IndexNow 提交已接受（HTTP 202）
- [x] Seznam IndexNow 提交已接受（HTTP 200）

## 需要你手动做一次（约 5 分钟）

Google 的 sitemap ping 接口已在 2023 年废弃，现在唯一可靠的方式是
Google Search Console 验证所有权。这一步必须真人操作，我无法代劳。

### 步骤

1. 打开 https://search.google.com/search-console
   用你的 Google 账号登录。

2. 左上角「添加资源」→ 选「网址前缀」→ 填入：
   https://lldaydayhappy.github.io/muse-invite/

3. 验证所有权 → 推荐用「HTML 标记」方式：
   - Google 会给你一段类似这样的标签：
     <meta name="google-site-verification" content="xxxx...">
   - 把 content 里那串值发给我，我把它写进 index.html 的 <head> 里
     并重新部署（1 分钟完成）。
   - 回到 GSC 点「验证」。

   备选（不用等我）：GitHub Pages 支持「域名提供商」验证，
   但 GitHub 不在 Google 的支持列表里，所以 HTML 标记最稳。

4. 验证通过后，左侧「站点地图」→ 添加：
   https://lldaydayhappy.github.io/muse-invite/sitemap.xml

5. 左侧「网址检查」→ 粘贴首页 URL → 点「请求编入索引」。
   这一步会让 Google 主动来抓，通常 1-7 天内收录。

## 关于收录速度

- Bing / Seznam / Yandex：已提交，通常 1-3 天
- Google：首次收录通常 3-14 天，之后长尾会持续来流量
- B站 评论里的链接：即时生效，真人点击不受搜索引擎影响

## 更新名额进度

页面支持 URL 参数动态显示剩余名额，无需改代码：

  https://lldaydayhappy.github.io/muse-invite/?used=12

把 12 换成实际已兑换人数即可。页面会自动算出「剩余 18 / 30」
并把进度条推到对应位置。真实消耗比「名额有限」四个字更能推动行动。

如需永久改默认值，告诉我数字，我改 index.html 里的 USED 变量并重新推送。
