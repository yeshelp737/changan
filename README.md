/*********************************

功能：Focos+解锁订阅
下载地址：https://is.gd/vpRvsM
软件版本：2.1.0
作者：changan
更新时间：2023-9-2

******************************

[重写本地]

^https?:\/\/.*\.oracle\.bendingspoonsapps\.com\/v\d\/(users\/.+|purchases\/verify) url script-response-body https://github.com/yeshelp737/changan/new/main?filename=README.md.js

[中间人]

主机名 = *.oracle.bendingspoonsapps.com

**************************************/


if ($response.body!= '未定义'){
var ojbk = JSON.parse($response.body);
const url = $request.url;

if (url.indexOf('splice') != -1) { ids = "com.path36.SpliceFree.1y_t150_bundle";}
if (url.indexOf('filmicpro') != -1) { ids = "com.cinegenix.filmic.pro.1y_t130_bundle_creator";}
if (url.indexOf('firstlight') != -1) { ids = "com.filmicpro.firstlight.1y_t130_bundle_creator";}
if (url.indexOf('doubletake') != -1) { ids = "com.filmicpro.doubletake.1w_t20_bundle_creator";}
if (url.indexOf('focos') != -1) { ids = "com.focos.1y_t130_bundle_creator";}
if (url.indexOf('remini') != -1) { ids = "com.bigwinepot.nwdn.international.1y_p99_99_ft_pro";}
if (url.indexOf('focoslive') != -1) { ids = "com.focoslive.1y_t130_adj";}
if (url.indexOf('thirtydayfitness') != -1) { ids = "com.vigorapps.30DayFitness.1y_t130_bundle_adj";}
if (url.indexOf('sleep') != -1) { ids = "com.bendingspoonsapps.SleepHelp.1y_t100_bundle_adj";}
if (url.indexOf('yoga') != -1) { ids = "com.flyingnayeem.yoga.1y_t100_1w_bundle_adj";}

ojbk["我"]["active_subscriptions_ids"] = [(ids)];
ojbk["我"]["active_bundle_subscriptions"] = [{
   “到期”：“2099-09-09T09:09:09+00:00”，
   “产品 ID”：（ID），
   “功能”：[“解锁”]
  }];
ojbk["设置"]["__identity__"]["过期"] = "2099-09-09T09:09:09+00:00";
$done({body : JSON.stringify(ojbk)});
}
