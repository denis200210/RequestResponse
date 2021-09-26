# Написать эссе, отражающее особенности как минимум 10 уникальных HTTP-заголовков для Request и Response.
  

На паре мы разобрали структуру, как работают сети, в процессе была затронута тема request и response. Теперь рассмотрим заголовки присущие Request и Response с помощью консоли разработчика в браузере на различных web-ресурсах.  

---



### github.com
При переходе на сайт https://github.com//, мы видим следующую картину:
![github.com](github.jpg)


**Request Headers**  

```css
:authority: github.com
:method: GET
:path: /denis200210
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: en,ru;q=0.9
cookie: _ga=GA1.2.1875612930.1585044399; _octo=GH1.1.2023794200.1616581584; user_session=PIMRVKGMsKuR8mrhg1n3mcZB2lrSVPvJEgkYW7lMuoIR6oMQ; __Host-user_session_same_site=PIMRVKGMsKuR8mrhg1n3mcZB2lrSVPvJEgkYW7lMuoIR6oMQ; logged_in=yes; dotcom_user=denis200210; color_mode=%7B%22color_mode%22%3A%22auto%22%2C%22light_theme%22%3A%7B%22name%22%3A%22light%22%2C%22color_mode%22%3A%22light%22%7D%2C%22dark_theme%22%3A%7B%22name%22%3A%22dark%22%2C%22color_mode%22%3A%22dark%22%7D%7D; tz=Asia%2FVladivostok; has_recent_activity=1; _device_id=84bb7b9863aae2acf52801f2a1495b02; _gh_sess=rYGeJUaDZkFHpXxVN1O2rfF3GR6PC5o%2Bw98yAGfFnIhmUtyHI4ICac7N7wNgQ%2FNtfwfyxtgkWiGCo92iKY33vWaAhWowKwTn8xH7quZP38%2B7ntTnYx5GDO2oza6UGO5qc03B4uyJuQiYJdzwLvMxcQCUBTcZCEDwCSH9on4P2pQ%3D--XJtgl0QElWkWFmzR--jDjwJ%2Bosph9XIDt1zItDzA%3D%3D
dnt: 1
if-none-match: W/"2726cf7cccfcc3db55381278d2a1dd04"
referer: https://github.com/denis200210/ddssd
sec-ch-ua: "Chromium";v="94", "Microsoft Edge";v="94", ";Not A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36 Edg/94.0.992.31
```

Мы видим, что пользователь пытается по домену github.com *(authority)* перейти по пути '/denis200210' *(path)*, выполняется метод GET *(method)*, протокол https *(scheme)*. 

Мы можем увидеть определение языковых предпочтений клиента *(Accept-Language)* это английский или русский. 

Также видим с какого устройства произведён переход и какой используется браузер + какие-то параметры браузера и движок, используемый им *(sec-ch-ua-platform и sec-ch-ua)*. Так же в параметре *accept-encoding* мы видим список форматов сжатия данных, таких как gzip, deflate, br, которые поддерживает клиент.  

Так как сайт нас сразу перебросил на главную страницу , то мы видим следующие заголовки:
```css
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
```

**Response Headers**
```css
cache-control: max-age=0, private, must-revalidate
content-encoding: gzip
content-security-policy: default-src 'none'; base-uri 'self'; block-all-mixed-content; child-src github.githubassets.com; connect-src 'self' uploads.github.com www.githubstatus.com collector.githubapp.com api.github.com github-cloud.s3.amazonaws.com github-production-repository-file-5c1aeb.s3.amazonaws.com github-production-upload-manifest-file-7fdce7.s3.amazonaws.com github-production-user-asset-6210df.s3.amazonaws.com cdn.optimizely.com logx.optimizely.com/v1/events translator.github.com wss://alive.github.com; font-src github.githubassets.com; form-action 'self' github.com gist.github.com; frame-ancestors 'none'; frame-src render.githubusercontent.com viewscreen.githubusercontent.com; img-src 'self' data: github.githubassets.com identicons.github.com collector.githubapp.com github-cloud.s3.amazonaws.com secured-user-images.githubusercontent.com/ *.githubusercontent.com; manifest-src 'self'; media-src github.com user-images.githubusercontent.com/; script-src github.githubassets.com; style-src 'unsafe-inline' github.githubassets.com; worker-src github.githubassets.com github.com/socket-worker-0af8a29d.js gist.github.com/socket-worker-0af8a29d.js
content-type: text/html; charset=utf-8
date: Sun, 26 Sep 2021 05:49:38 GMT
etag: W/"52c46e1332da044649d9627414b14537"
expect-ct: max-age=2592000, report-uri="https://api.github.com/_private/browser/errors"
permissions-policy: interest-cohort=()
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
server: GitHub.com
set-cookie: has_recent_activity=1; path=/; expires=Sun, 26 Sep 2021 06:49:37 GMT; secure; HttpOnly; SameSite=Lax
set-cookie: _gh_sess=xImGBYx3Ao2xOmqOkXO9kByPo1gWRVxDw7r5vn17swnVoiQzvcXIuk1UjrNiv7k02BOg97iqpakra3NBlX%2Fd6HNv%2FlhIxYyCPWWZI1eRDFIZN56XVhFf5L8pTkGr6C5skvcwArGlya0opnabuaUpQjP0demVBaVtqGPgqSS65IThfSFVVG9xSubij1eR4RkQek2L%2Ffr3ep2dPxUoo1Yh4er8xKtpNjrqY2Zk4s9Z0tvg%2FTFFdhW4gs1O7BPscjqiA22SUYSz4F%2Fa%2FYdVMqD4Nhdt6GTm5JcNOh%2BXUSfuc9aNI7II1P2RdwDFEl1ddJpfbEQ4sh8ZFiCO8cO0DzSEYYVGwgkaiTHx9G%2B6Y8ZPPWSRjHQYmv6hl6vjUgIj%2BdJWmiW6PmJi2vFdXmRlIgyQoZTqRnGV%2FTo3zNdr83bAlPXt0lahXO5SIy8CDRhZaBX%2Bv3GIcdMHobAFmUXJ4pzNfytKquSn31Y0ays3RDoGwZMTd4eR8859%2Bc7oQo68%2FQRPIQfchOfveWy9pYYOOM%2BYjXNYe8b39xDzBTml%2BaXHh0K%2BPMdA0JYSZFAR91hGAPBbaHHppdpVOZUmwz6MamAXbRykcU1HW%2BoGbCASaFxfHOiqgEfzcU2wXnPj7h0q2wXO5%2FUwE%2BKPu4d3QoVLZs2IfSH16pobe9QIJkJ1gGXQPic%3D--anfUYNAf5gZxoNeQ--JZjhSxPMxkLT40s5T2nqaw%3D%3D; path=/; secure; HttpOnly; SameSite=Lax
strict-transport-security: max-age=31536000; includeSubdomains; preload
vary: X-Requested-With, X-PJAX-Container
vary: Accept-Encoding, Accept, X-Requested-With
x-content-type-options: nosniff
x-frame-options: deny
x-github-request-id: 369A:21DE:142620D:1505DE3:615009F0
x-xss-protection: 0
```
Здесь мы так же можем заметить в кодировке присутствует алгоритм сжатия, но теперь только один - gzip. Так как, нас всегда при переходе на главную страничку GitHub перебрасывает на обзор. 

Так же мы видим MIME тип документа *(Content-Type)* - тип контента: text/html и его кодировку windows-1251. Так же мы можем видеть полную дату и время создания сообщения *(date)* и заданные при переходе на сайт куки. Так же можно узнать сервер *(server)*, с которого пришёл запрос - GitHub.com. 

Имеется заголовок *Content-Security-Policy*, управляющий ресурсами, которые пользовательскому агенту разрешено загружать для данной страницы. 

Заголовок HTTP-ответа *X-Frame-Options* может использоваться, чтобы указать, следует ли разрешить браузеру отображать страницу в ```<frame>, <iframe>, <embed>``` или ```<object>```. В нашем случае указан параметр DENY, т.е. браузер будет пытаться загрузить страницу во фрейме, но не только при загрузке с других сайтов, но и при загрузке с того же сайта. Заголовок ответа HTTP *X-XSS-Protection* - это функция Internet Explorer, Chrome и Safari, которая останавливает загрузку страниц при обнаружении атак с использованием отраженных межсайтовых сценариев (XSS). В нашем случае:
```css 
x-xss-protection: 0
```
В нашем случае фильтр выключен.

---

### https://www.dns-shop.ru//
![dns-shop.ru](dns.ipg)
**Request Headers**  
```css
DNT: 1
Referer: https://www.dns-shop.ru/
sec-ch-ua: "Chromium";v="94", "Microsoft Edge";v="94", ";Not A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36 Edg/94.0.992.31User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.82 Safari/537.36
```
*DNT* — это HTTP-заголовок, позволяющий обойти отслеживание ваших действий сайтами.DNT в настоящее время принимает три значения: 1 означает, что пользователь не хочет, чтобы его отслеживали, 0 означает, что пользователь соглашается на отслеживание, и null (по умолчанию) означает, что пользователь не выражал предпочтения. В нашем случае значение 1.

Заголовок запроса *sec-ch-ua-platform* указывает на какой платформе просматривается, в данном случае Windows.  

Заголовок запроса HTTP *Upgrade-Insecure-Requests* отправляет сигнал на сервер, выражающий предпочтение клиента зашифрованного и аутентифицированного ответа, и что он может успешно обрабатывать директиву CSP upgrade-insecure-requests. На сайте dns-shop он принимает значение 1, т.е. запрос клиента сигнализирует серверу, что он поддерживает механизмы обновления для обновления небезопасных запросов(upgrade-insecure-requests).  

**Response Headers**  
```css
Cache-Control: no-store, no-cache, must-revalidate
Connection: keep-alive
Content-Encoding: br
Content-Language: ru
Content-Security-Policy: default-src 'self' 'unsafe-inline' 'unsafe-eval' https://dns-shop.ru https://*.dns-shop.ru https://chat.dns-shop.ru:8080 https://cdn.retailrocket.ru https://widget.cloudpayments.ru/  https://*.retailrocket.net https://*.yadro.ru https://webvisor.com https://bs.yandex.ru https://yandex.ru https://mc.yandex.ru  https://metrika.yandex.ru https://yastatic.net https://*.yandex.st https://yandex.st https://awaps.yandex.ru https://reviewthree.com/ https://*.maps.yandex.net https://google-analytics.com https://*.google-analytics.com https://googleadservices.com https://*.googleadservices.com  https://*.google.ru https://google.ru https://*.google.com https://google.com https://google.ie https://*.google.ie  https://gstatic.com  https://*.gstatic.com https://www.googletagmanager.com/ https://www.youtube.com/ https://youtube.com/ https://content.24ttl.stream https://doubleclick.net https://*.ok.ru https://ok.ru https://*.mail.ru https://mail.ru https://vk.com https://*.vk.me https://*.mycdn.me  https://mycdn.me https://begun.ru https://*.begun.ru https://vsegda-da.com https://newrelic.com https://*.newrelic.com https://bam.nr-data.net  https://static.criteo.net https://sslwidget.criteo.com/ https://dis.eu.criteo.com/dis/ https://eu-sonar.sociomantic.com/ https://logo.flixfacts.co.uk/ https://media.flixsyndication.net/ https://*.flix360.com/ https://*.flix360.io/ https://assets.delvenetworks.com/  https://s.delvenetworks.com/ https://dev-origin.flixsyndication.net/ https://d2m3ikv8mpgiy8.cloudfront.net/ https://d3nkfb7815bs43.cloudfront.net/  https://d15mv1adrb1s6e.cloudfront.net/ https://www.lg.com/ https://*.webcollage.net https://content.syndigo.com https://ams.creativecdn.com/ https://i.s-microsoft.com/ https://cdn.ampproject.org/ https://s7.addthis.com/ https://m.addthisedge.com/  https://m.addthis.com/ https://bot.aimylogic.com/ https://fonts.googleapis.com https://cdn.diginetica.net/ https://tracking.diginetica.net/  https://connect.facebook.net/ https://zingaya.com/widget/ https://d1bvayotk7lhk7.cloudfront.net https://creativecdn.com/ https://ssl.p.jwpcdn.com/ intent://arvr.google.com https://*.doubleclick.net https://api-maps.yandex.ru https://maps.yandex.net  https://assets-jpcust.jwpsrv.com/ https://www.youtube.ru/ https://youtube.ru/ https://s.ytimg.com/ https://*.go-mpulse.net/  https://gum.criteo.com/ https://media.flixfacts.com/ https://media.flixcar.com https://content.jwplatform.com/ https://media.pointandplace.com/  https://player.pointandplace.com/ https://analytics.tiktok.com/ https://dv-proxy-asmsys.dns-shop.ru:17589/ https://suggest-maps.yandex.ru https://www.youtube-nocookie.com/ ; img-src * data:; font-src * data:; media-src blob: https://media.flixcar.com/ https://*.webcollage.net/ https://content.24ttl.stream/ https://*.flix360.io/ https://www.youtube-nocookie.com/; connect-src 'self' https://*.dns-shop.ru https://*.retailrocket.net https://ohio8.vchecks.me https://hls-jp.jwpsrv.com/ https://content.jwplatform.com/  https://mc.yandex.ru/ https://www.google-analytics.com/ https://*.mtproxy.yandex.net/ https://bam.nr-data.net https://api.retailrocket.net  https://content.syndigo.com/ https://google-analytics.bi.owox.com/ https://api-maps.yandex.ru/ https://stats.g.doubleclick.net/  https://www.google.com/ads/ https://m.addthis.com/live/red_lojson/ https://s7.addthis.com/l10n/ https://top-fwz1.mail.ru/  https://bot.aimylogic.com/restapi/ wss://chat.dns-shop.ru https://chat.dns-shop.ru https://e-shop.homecredit.ru https://media.pointandplace.com/ https://vk.com https://media.flixcar.com/ https://autocomplete.diginetica.net/ https://www.facebook.com/tr/ wss://adm-ups-dev-chat.dns-shop.ru/  https://adm-ups-dev-chat.dns-shop.ru/ http://webapi.south.dns-shop.ru/ http://webapi.zenit.dns-shop.ru/ https://webapi.zenit.dns-shop.ru/  https://backend.zenit.dns-shop.ru https://analytics.tiktok.com/ https://dv-proxy-asmsys.dns-shop.ru:17589/ https://content.24ttl.stream/  https://*.flix360.io/ http://shops.dns-shop.ru/ https://www.youtube-nocookie.com/  https://firebaseinstallations.googleapis.com/ https://fcmregistrations.googleapis.com/ ; frame-src 'self' intent: https://e-shop.homecredit.ru https://*.fls.doubleclick.net/ https://club.dns-shop.ru https://eu-sonar.sociomantic.com/ https://widget.cloudpayments.ru/ https://content.24ttl.stream/  https://reviewthree.com/ https://media.flixfacts.com/ https://media.flixcar.com/ https://d3nkfb7815bs43.cloudfront.net/ https://gstatic.com  https://www.google.com https://optimize.google.com https://ftp.dexp.club https://www.facebook.com/ intent://arvr.google.com https://ssl.p.jwpcdn.com/  https://d15mv1adrb1s6e.cloudfront.net/ https://media.pointandplace.com/  https://content.jwplatform.com/ https://assets-jpcust.jwpsrv.com  https://media.flixsyndication.net/ https://t.flix360.com/ https://Syndication.flix360.com/ https://*.flix360.com/ https://ftp.dns-shop.ru/ https://www.youtube.com https://api-maps.yandex.ru/  http://d2m3ikv8mpgiy8.cloudfront.net https://player.pointandplace.com/ https://t.pointandplace.com/ https://d3np41mctoibfu.cloudfront.net/ https://*.flix360.io/ https://www.youtube-nocookie.com/
Content-Type: text/html; charset=UTF-8
Date: Sun, 26 Sep 2021 08:25:01 GMT
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Keep-Alive: timeout=60
Link: <https://as.dns-shop.ru/assets/c097a383/jquery.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/7e118f26/themes/base/jquery-ui.min.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/7e118f26/jquery-ui.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/7e118f26/jquery-ui-compatibility-hacks.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/theme.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/theme/custom.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/theme/header/desktop.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/1962a38/yii.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/forms.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/1962a38/yii.activeForm.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/1962a38/yii.validation.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/1d4a722/deffer-css.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/8e1191d5/polyfill.min.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/9a9c14d4/lazyload.min.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/theme/widgets/loading-bar.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/common/widgets/loading-bar.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/common/components/cart-refresh-service.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/layout.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/helpers.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/common.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/modules.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/f831350a/homepage-grid.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/f831350a/homepage-grid.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/e4cde37e/menu-desktop_ph.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/699925ab/menu-mobile_ph.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a6c98572/tiny-slider.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a6c98572/min/tiny-slider.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/e2f2017f/homepage-actual-offers-main.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/2a36d479/homepage-benefits__md-min.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/container-ns.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/modules/pwa-sw-wrapper.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/modules/log-action.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/common/components/retail-rocket.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/ac675654/header-mobile.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/ac675654/header-mobile.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/acee0398/modal.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/acee0398/modal.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/theme/widgets/city-select.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/common/widgets/city-select.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/9d7ac1d3/input-search.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/9d7ac1d3/input-search.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/d620d903/tooltip.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/d620d903/tooltip.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/f4a1093d/button.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/f4a1093d/button.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/b35cfbd6/links.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/b35cfbd6/links.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/a50ecd56/presearch.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a50ecd56/presearch.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/theme/widgets/menu-dropdown.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/common/widgets/menu-dropdown.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/cb581a77/cart-link__md-min.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/dbc29694/cart-front-repository.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/f7cbb9cb/app-cart-modal.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/f7cbb9cb/app-cart-modal.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/f029bbc1/user-notify.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/f029bbc1/user-notify.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/8774a6a2/user-notification.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/common/components/footer.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/83611419/outdated-browsers-notification.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/83611419/outdated-browsers-notification.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/9fc57beb/scroll-top.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/9fc57beb/scroll-top.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/191d3c53/feedback-modal-widget.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/191d3c53/feedback-modal-widget.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/185af124/textarea.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a440a024/subscription.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a440a024/subscription.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/d75203d/button-install-pwa.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/d75203d/button-install-pwa.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/55d0e729/bottom-navbar_ph.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/a3b9c367/compare-storage.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/css/modules/ajax-state/ajax-state.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/modules/ajax-state/processors/compare-link.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/modules/ajax-state/processors/wishlist-link.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/css/modules/ajax-state/processors/opinion-notifications.css>;rel=preload;as=style, <https://as.dns-shop.ru/assets/bfdd2391/js/modules/ajax-state.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/modules/ajax-state/processors/opinion-notifications.js>;rel=preload;as=script, <https://as.dns-shop.ru/assets/bfdd2391/js/modules/ajax-state/processors/chatik.js>;rel=preload;as=script
Pragma: no-cache
Server: nginx
Transfer-Encoding: chunked
Vary: Accept-Encoding
X-Content-Type-Options: nosniff
X-Host: dns-shop
X-VARITI-CCR: 307100066:86
X-XSS-Protection: 1; mode=block
```
Заголовок *Cache-Contro* используется для задания инструкций кеширования как для запросов, так и для ответов.

Так же можно заметить заголовок *Link*, который определяет отношения между текущим документом и внешним ресурсом.

---

На выходе мы наулись работать с HTTP протоколом. Рассмотрев заголовки  Request и Response  с помощью консоли разработчика в браузере в различных web-ресурсах, саметили что сайты уникальные сами по себе. На одном сайте одни заголовки, а на других другие, но все есть схожести.
