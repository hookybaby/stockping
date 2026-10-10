# StockPing · 到货啦

**Apple Store iPhone 门店取货库存查询、到货监控与提醒。支持 macOS 和 Windows。**

[官方网站](https://stockping.plegle.uk) · [下载最新版](https://github.com/hookybaby/stockping/releases/latest) · [问题反馈](https://github.com/hookybaby/stockping/issues)

StockPing 帮你查询指定 Apple Store 的 iPhone 取货库存。免费版可以手动查询；购买 Standard 或 Pro 后，可持续监控你选择的「门店 × 机型配置」，并在发现到货时发送提醒。它在你的电脑上运行，不代购、不自动提交订单，也不保证库存保留到结账。

当前版本：**0.2.17**。免费版仅提供查询，添加和运行到货提醒需要付费授权。

0.2.13 加强授权复检、设备密钥绑定与时钟回拨检测。启动及正常每小时联网验证，凭证有效 3 小时，另有 24 小时断网宽限；到期暂停付费监控并保留数据。Standard 为 5 个、Pro 为 50 个监控组合，一次性购买价格不变。

0.2.14 修复更换激活码时的设备占用：已有授权须先解绑本机，再激活新码，监控数据保留。配套服务修复重复付款、退款与邮件并发处理，并支持争议胜诉后的管理员审核恢复。

0.2.15 修复查询结果表格右侧容量列被遮挡的问题，门店名称随列宽换行，四个容量列可同时查看。

0.2.16 支持 Chrome、Edge 和 Safari 购买准备扩展：一次安装后，点击“购买此配置”自动选择不换购、不加 AppleCare+，并定位加购按钮。

0.2.17 配合扩展 1.1.0，新增可选的自动加购和结账入口。沿用有货门店，多门店先选择；每步等待最多 2 分钟，加购只执行一次。购物袋有其他商品或门店不匹配时暂停，登录、取货信息、提交订单和付款由你完成。大陆流程已逐步实测；其他地区有差异，无法识别时需手动继续，台湾和新加坡的自动流程尚未支持。

## 下载与安装

| 平台 | 下载文件 | 适用设备 |
| --- | --- | --- |
| macOS | [StockPing-0.2.17-arm64.dmg](https://github.com/hookybaby/stockping/releases/download/v0.2.17/StockPing-0.2.17-arm64.dmg) | 仅 Apple 芯片（M 系列），macOS 13 及以上；不支持 Intel Mac |
| Windows 安装版 | [StockPing.Setup.0.2.17.exe](https://github.com/hookybaby/stockping/releases/download/v0.2.17/StockPing.Setup.0.2.17.exe) | Windows 10 / 11，64 位 x64 |
| Windows 便携版 | [StockPing-0.2.17-portable.exe](https://github.com/hookybaby/stockping/releases/download/v0.2.17/StockPing-0.2.17-portable.exe) | 无需安装，适合临时使用 |

macOS：打开 DMG，将 StockPing 拖入「应用程序」，再从「应用程序」启动。macOS 应用及 DMG 均完成 Developer ID 签名和 Apple 公证。

Windows：运行安装包，按提示选择安装位置；或下载便携版直接运行。Windows 包暂未提供代码签名，系统可能显示 SmartScreen 提示。请只从本项目 Release 下载，并核对该版本的 SHA-256 校验文件。

更新入口位于「关于」页面版本号旁的「检查更新」。下载完成并成功打开安装包后，应用会保存数据并自动退出，按安装向导完成更新；macOS 需将新应用替换到「应用程序」。更新前建议在设置中导出备份。卸载、换机或切换便携版前，也请先备份数据。

浏览器扩展 **1.1.0**（需单独安装）：

- [Chrome / Edge 扩展下载](https://stockping.plegle.uk/StockPing-Chrome-Edge-Helper-1.1.0.zip)：解压后安装；更新时覆盖原扩展文件夹，并在扩展管理页点击“重新加载”。
- [Safari 扩展下载](https://stockping.plegle.uk/StockPing-Safari-Helper-1.1.0.zip)：解压后将 StockPing Purchase Helper.app 放入“应用程序”；更新时替换同名应用，再在 Safari 设置中启用扩展并允许访问 Apple 网站。

[官网安装说明](https://stockping.plegle.uk/#browser-helper)。Safari 辅助应用支持 Apple 芯片和 Intel Mac，macOS 13 及以上。为兼容旧版主程序的更新识别，扩展 ZIP 由官网提供，不列为主程序安装包附件。库存查询主应用目前仍仅支持 Apple 芯片。

## 免费版、Standard 与 Pro

两个付费版本均为**一次性付款，无自动续费**。使用 Stripe 收款，授权由云端验证。

| 功能 | 免费版 | StockPing Standard | StockPing Pro |
| --- | --- | --- | --- |
| 价格 | HK$0 | **HK$49.90，一次性** | **HK$99.90，一次性** |
| 手动查询库存 | 支持 | 支持 | 支持 |
| 中国大陆跨城市查询 | 支持，无需代理 | 支持，无需代理 | 支持，无需代理 |
| 门店、机型与 SKU 管理 | 支持 | 支持 | 支持 |
| 添加、启用和运行到货提醒 | 不支持 | 支持 | 支持 |
| 监控组合数量上限 | 0 | **5** | **50** |
| 桌面到货通知 | 不支持 | 支持 | 支持 |
| 八个外部通知渠道 | 可保存未启用配置 | 全部支持 | 全部支持 |
| 同时授权设备数 | — | **1 台** | **1 台** |

**一个监控组合 = 一个地区的一家门店 + 一个 SKU。** 例如，同一家店的银色 256GB 和银色 512GB 占两个组合；同一 SKU 在两家店监控，也占两个组合。

Standard 和 Pro 的通知渠道相同；Pro 提供更多监控组合。Standard 升至 Pro 目前需要单独购买 HK$99.90 的 Pro 授权，**不自动抵扣 Standard 费用**。

如果解绑、退款、授权撤销或离线宽限期结束，软件会回到免费版。已有提醒和历史数据保留，但自动监控与通知暂停；重新取得有效付费授权后才能恢复。应用启动和正常每小时联网验证。签名凭证有效 3 小时，另有 24 小时断网宽限，即最后成功验证后最长 27 小时；恢复网络后可在设置中重新验证，无需再次购买。请升级至 0.2.16，以获得新的设备校验和授权期限规则。

## 软件功能

### 1. 库存查询

- 支持中国大陆、中国香港、中国台湾、日本、新加坡、美国六个地区。
- 内置 340 家门店和 240 个地区 SKU 的基础数据，可同步或自行维护。
- 按省份、城市或关键词查找门店，可同时选择多家门店。
- 按机型、颜色和容量选择需要查询的配置。
- 库存矩阵按「颜色 × 容量」展示，并列出有货门店；也可查看门店维度的结果。
- 区分「有货」「无货」「未知」与请求失败，不把未返回结果或网络错误当成无货。
- 中国大陆可直接查询其他城市的 Apple Store，无需为每个城市配置代理。
- 查询有货后可点击「购买此配置」，直接打开对应地区的 Apple 型号、颜色和容量购买页，减少重新选配置的步骤；目录信息不足时打开型号页。监控列表与到货自动打开也使用同一入口。取货门店和付款仍在 Apple 浏览器页面完成，库存以结账页为准。

Apple 的库存随时可能变化。其他地区的可查询范围取决于 Apple 接口实际返回的门店；没有确认结果时会显示「未知」。

### 2. 我的提醒与自动监控（Standard / Pro）

- 点击「准备添加监控」，逐项选择所需的「门店 × SKU」组合。
- 添加前查看每个组合的库存状态，支持搜索过滤、全选、清空选择和仅勾选有货项。
- 已监控的组合会标出，避免重复添加；超出方案额度时提示上限。
- 默认每 30 秒查询一轮，可在设置中调整间隔；失败时逐步延长重试间隔。
- 在「我的提醒」查看运行状态、下一轮时间、最近查询结果和各组合状态。
- 支持立即检查、启动或停止监控、单项启用或停用，以及删除或清空提醒。
- 软件可在托盘后台运行，并按设置开机启动；电脑关机、睡眠或软件退出时不会继续监控。
- 免费版的新增、重新启用和监控启动由主进程限制，托盘及开机自启也遵守授权状态。

### 3. 到货通知（Standard / Pro）

支持桌面系统通知，以及以下八个自定义渠道：

| 渠道 | 用途与配置 |
| --- | --- |
| Telegram | Bot Token 与 Chat ID |
| 飞书机器人 | Webhook，可选签名密钥 |
| 邮箱 | SMTP，支持 SSL / STARTTLS 与登录认证 |
| WhatsApp | WhatsApp Cloud API |
| Bark | iOS 推送，支持官方或自建服务 |
| 企业微信机器人 | 群机器人 Webhook |
| 钉钉机器人 | Access Token，可选加签密钥 |
| 通用 Webhook | 自定义 POST JSON 与鉴权请求头 |

- 多个渠道可同时启用，并可分别发送测试通知。
- 未启用时也可保存输入的渠道配置；免费版可以准备配置，购买后再启用。
- 敏感字段加密保存在本机，输入框的小眼睛可显示或隐藏已保存内容。
- 支持提醒冷却时间，减少重复推送。
- 支持跨午夜的免打扰时段：继续记录库存变化，暂停通知和自动打开购买页。
- 可设置发现到货时自动打开购买页；最终下单仍由用户在浏览器完成。
- 点击单项到货通知直达对应配置；同时到货多项时可选择具体型号与门店。
- 在监控行设置购买优先级（1 最高，未设置排后）；同一批结果按优先级选择自动打开的配置，不等待其他城市。
- 手机消息包含各配置购买链接；Bark 通知点击打开优先配置。
- 「购买准备」可提前打开 Apple 登录页、购物袋和准确配置，保存明确购买预设并导出辅助书签。书签目前仅支持中国大陆、一个配置与一家门店；无货、型号不符、门店不符或页面结构变化时停止并提示手动操作。加入购物袋不等于预留库存。

通知渠道可能需要你自行创建机器人、配置 SMTP 或购买第三方服务；这些服务的费用不包含在软件价格中。

### 4. 机型库与门店数据

- 查看和管理机型、颜色、容量及 Apple 商品编号（partNumber）。
- 从 Apple 购买页提取商品编号，或手动新增 SKU。
- 支持 JSON 导入、导出与内置数据恢复。
- 不同地区有独立的门店和商品编号，切换地区不会将原地区数据混用。

### 5. 提醒记录与补货规律

- 查看到货、售罄、通知发送和查询异常记录。
- 搜索、筛选记录并导出 CSV。
- 根据本机记录查看到货时段、门店补货频率及有货持续时间等统计。
- 统计依赖你的监控历史；它不是 Apple 的补货计划，也不预测或保证未来库存。

### 6. 设置与诊断

「版本与购买」位于设置最上方，可直接购买、输入邮箱收到的激活码、复检授权或解绑设备。

- 简体中文、繁体中文、英文界面，可随时切换。
- 配置查询间隔、并发、超时、通知冷却和免打扰时段。
- 配置开机启动、关闭到托盘和最小化行为。
- 可选代理设置；Windows 未填写自定义代理时使用系统网络代理配置。
- 导出和导入备份，恢复监控、目录及设置；授权凭证不作为可迁移备份绕过设备绑定。
- 提供网络诊断和诊断报告导出，便于反馈连接问题。
- 在「关于」检查和下载新版本。

## 第一次使用

1. 下载并启动软件，在「库存查询」选择地区、门店、机型和容量。
2. 点击「查询现货」查看结果。免费版可以完成这一步。
3. 如需到货提醒，进入「设置 → 版本与购买」，购买 Standard 或 Pro，输入邮件中的激活码。
4. 回到库存查询，点击「准备添加监控」，勾选所需组合并确认添加。
5. 在「我的提醒」启动引擎，配置桌面通知或自定义通知渠道，并保持软件与网络运行。
6. 在「购买准备」确认目标配置和门店，提前在自己的浏览器登录 Apple 账户，准备好收货信息和付款方式。
7. 收到提醒后，打开 Apple 购买页确认最新库存并自行结账。

联系开发者与购买售后：[support@plegle.uk](mailto:support@plegle.uk)。

## 购买、激活与换机

可从[官网](https://stockping.plegle.uk/#pricing)或软件设置发起购买。打开付款页不会锁定版本，也不会激活授权。

1. 选择 Standard 或 Pro，在 Stripe 结账页填写并核对收码邮箱。
2. 完成一次性付款；服务器确认到账后，将激活码发送至该邮箱。
3. 检查收件箱和垃圾邮件，在「设置 → 版本与购买」输入激活码。
4. 首次激活时才绑定电脑，不需要注册账号。

**新购买的 Standard 和 Pro 都是一枚码同时绑定一台电脑。** 换机前在旧电脑点击「解绑本机」，再到新电脑输入同一个码。旧电脑无法使用时，联系支持核实购买后重置绑定。历史双设备授权保留原设备数量。旧版已创建的订单，在新版中仍可通过「恢复旧版购买」领取。

### 已付款但没有收到码或激活失败

- 检查 Stripe 填写的邮箱和垃圾邮件；延迟付款确认或邮件处理可能需要时间，**不要重复付款**。
- 邮箱填错时，请私下向 [support@plegle.uk](mailto:support@plegle.uk) 提供 Stripe 收据或付款编号、原邮箱和正确邮箱。核实购买后可补发原激活码，无需重新购买；仅提供一个新邮箱无法领取别人的授权。
- 保留 Stripe 收据或付款编号、收码邮箱和错误提示，联系支持核实。
- 开发者可查询邮件提交状态、补发同一个激活码、重置绑定或撤销授权；补发不产生第二份授权。
- 完整退款或争议会撤销对应授权，联网验证后停止付费功能；离线电脑不会立即收到撤销状态。
- 在公开 Issues 中只描述问题，**不要公开激活码、收据、邮箱或通知渠道密钥**。

## 隐私与数据

库存结果、门店与机型数据、提醒记录和设置保存在本机。敏感通知配置加密保存，备份文件仍应自行妥善保管。用户端备份中的凭据由系统安全存储加密，与授权服务端的数据库备份及密钥相互独立；普通设置、监控和历史仍为可读 JSON。系统安全加密不可用时，不会导出包含明文凭据的备份。

软件向 Apple 请求库存；外部通知只发往你配置的渠道。Stripe 收集付款邮箱并处理付款，软件不读取银行卡信息。授权服务保存付款与邮箱用于发码和售后；Oqumail 接收收件邮箱及激活码以发送邮件。激活和验证时，软件向授权服务发送激活码、机器指纹和授权凭证。不需要注册 StockPing 账号。Apple 账户登录仅在你自己的浏览器和 Apple 官方网页完成；本应用不会读取、保存或代填 Apple 账号与密码。

## 常见问题

**为什么显示「未知」？**

Apple 没有返回可确认的门店库存，或请求失败。未知不代表无货，可稍后重试并查看诊断。

**为什么 Windows 和 Mac 结果不同？**

先检查两台设备的地区、门店、SKU 和网络是否一致；Windows 会继承系统代理配置。网络出口及 Apple 响应范围可能不同，中国大陆跨城查询已支持直接查询。请保留错误提示或导出诊断报告。

**提前登录 Apple 账户会泄漏密码吗？**

点击登录按钮只会在你自己的浏览器打开 Apple 官方登录页。StockPing 不接触登录表单，不读取、保存或代填账号与密码，也不接管浏览器会话。提前登录可减少到货后结账时的登录步骤；请在 Apple 官方网页完成登录。

**免费版为什么不能添加提醒？**

免费版用于手动查询；持续监控、桌面到货通知和外部通知属于 Standard / Pro 功能。

**我能在云端一直监控吗？**

不能。云端仅处理付款和授权，库存监控运行在你的电脑上。关机、睡眠或退出软件后监控停止。

**提醒到了，为什么下单时没货？**

库存可能在两次查询之间变化，也可能被其他用户买走。软件只能报告查询时的结果，不能锁定库存。

**付款后会自动续费吗？**

不会。Standard 为 HK$49.90 一次性，Pro 为 HK$99.90 一次性。

**这是 Apple 官方软件吗？**

不是。StockPing 是独立工具，与 Apple Inc. 无隶属关系。

## English overview

StockPing checks iPhone pickup availability at Apple retail stores on macOS and Windows. It supports Chinese Mainland, Hong Kong, Taiwan, Japan, Singapore and the United States, with Simplified Chinese, Traditional Chinese and English interfaces.

Free supports manual and cross-city stock queries only. Adding alerts, automatic monitoring and restock notifications require a paid license:

- **Standard: HK$49.90 once** — 5 store × SKU combinations, one device.
- **Pro: HK$99.90 once** — 50 combinations, one device.
- Both include desktop notifications and all eight external channels. No recurring billing.

Purchase from the website or **Settings → Plans & purchase**, enter your email at Stripe checkout, then activate in the app with the emailed code. Keep the code private. Unbind the old computer before moving it. If payment succeeded but activation did not, keep the Stripe receipt, payment reference and error message, and contact [support@plegle.uk](mailto:support@plegle.uk) without paying again.

Monitoring runs locally and requires the computer, app and network to remain active. StockPing cannot reserve stock or place orders. Apple responses may be incomplete; unknown availability is never treated as out of stock.

[Website](https://stockping.plegle.uk) · [Latest release](https://github.com/hookybaby/stockping/releases/latest) · [Report a problem](https://github.com/hookybaby/stockping/issues)

From 0.2.13, licenses are checked on startup and normally hourly. Signed credentials last three hours, followed by a 24-hour offline grace period; monitoring pauses after expiry and keeps your data. Verification does not charge you again.

Version **0.2.17** supports Apple silicon Macs running macOS 13 or later and Windows 10 / 11 x64. Intel Macs are not supported. Sign in to your Apple account ahead of time in your own browser for faster checkout. Sign-in takes place only on Apple’s official website; StockPing never reads, stores or fills in your Apple account or password.
