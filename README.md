# DMIT 怎么样：Pro、Eyeball、Tier 1 三条线路差在哪，价格、退换政策与选购建议一次说清

搜「DMIT 怎么样」的人，通常已经翻过一轮 VPS 推荐帖，然后卡在同一个地方：这家的评价完全对不上。一边说线路稳得离谱、晚高峰一条直线；另一边说贵得没道理、库存抢不到、IP 拿到手就是墙的。

两拨人说的都成立，因为他们买的根本不是同一个东西。DMIT 在同一个机房里同时卖三档网络（Pro / Eyeball / Tier 1），价格能差好几倍，体验自然也对不上号。

## 先把结论摆出来

**适合买 DMIT 的情况：**

- 网站、跨境业务的用户主要在中国大陆，且不接受晚高峰掉速
- 需要一台当"贴身机器"用的中转或落地，长期挂着不想折腾
- 预算在每月 10 美元以上，愿意为线路和硬件多付一点
- 想用支付宝付款、能说中文工单沟通

**不太适合的情况：**

- 只想花几美元/月，那 Tier 1 甚至别家更便宜的机器更合适
- 业务全在海外，不涉及大陆访问——买 Pro 属于纯浪费
- 喜欢囤一堆低配机器跑批量任务，DMIT 的库存和单价都不支持这种玩法

一句话概括这家的定位：它不是拼最低价的商家，是拿线路质量换溢价的商家。

## DMIT 是谁，「大妈」这个外号哪来的

DMIT 是一家 2017 年前后成立的美国公司，主营 KVM 架构的云实例（也就是常说的 VPS）和更高阶的裸金属产品，机房分布在洛杉矶、香港、东京三地。中文圈叫它「大妈」，纯粹是 dmit 四个字母念快了顺口，不是官方中文名。

硬件上全线用 AMD EPYC 处理器，平台代号按代际区分：AS3 对应 EPYC 7003、AN4 对应 9004、AN5 对应 9005。现在洛杉矶和香港的主力是 AN5，AS3 作为更便宜的一代还在卖。付款支持支付宝、PayPal 和信用卡，有中文客服——这两点对国内用户的实际意义，比参数表上的跑分大得多。官方一直强调不超售，这也是它敢把单价比同类产品抬高一截的底气。

## Pro / Eyeball / Tier 1：三档网络的真实区别

选 DMIT 的第一步不是挑配置，是挑线路。同样 2 核 2G，Pro 和 Tier 1 的价差可能有三四倍，钱全花在回国的路由上。

| 档次 | 大陆方向路由 | 适合谁 | 价格档位 |
| --- | --- | --- | --- |
| Premium（.Pro） | IPv4 三网 CN2 GIA，IPv6 走 9929 / CMIN2 | 对延迟和晚高峰稳定性有硬要求 | 最高 |
| Eyeball（.EB） | IPv4 与 IPv6 都走 9929 / CMIN2 | 预算有限但不想用普通线路 | 中等 |
| Tier 1（.T1） | 纯国际 BGP，无中国专项优化 | 海外业务、备份、CI/CD、中转节点 | 最低 |

判断逻辑其实很直白：电信用户对 CN2 GIA 的感知最明显，选 Pro 值；移动和联通用户在 EB 上能拿到 CMIN2 和 9929，性价比更高；至于 Tier 1，路由完全不优化，大陆访问延迟可能比一些绕路的机器还难看——它是给不碰国内流量的场景准备的。

**测试 IP 和 Looking Glass 官网都有**，买之前 ping 一下自己所在运营商的表现，比看十篇测评都有用。

## 三个机房怎么选

第三方测评里比较一致的延迟数据：香港 Pro 三网平均在 43ms 上下（电信 42ms、联通 42ms、移动 46ms），洛杉矶 Eyeball 平均约 160ms，洛杉矶 Tier 1 平均约 208ms。东京介于香港和洛杉矶之间。

香港的物理距离优势换不来便宜——HKG.Pro 起步就是每月 39.9 美元，是洛杉矶同档的好几倍。所以：

- 港内业务、对延迟极度敏感、预算充足 → 香港
- 大部分建站和跨境场景 → 洛杉矶，性价比最高
- 需要东亚节点但嫌香港贵 → 东京（注意东京 Eyeball 系列已经下线，现在主要是 Pro 和 Tier 1）

## 套餐和价格参考

DMIT 官网在售的 SKU 有几十个：三个机房 × 三条线路 × 多代平台，还叠加了限量特价机。下面按机房整理的是能交叉核对到的主力规格。

价格和库存变动很频繁——平台换代、下架、补货都会影响，实际下单请以购物车显示的金额为准。

### 洛杉矶 LAX（Pro / CN2 GIA）

AS3 平台价格更低，AN5 平台硬件更新。两代同时在售，同一个套餐名下价格并不统一。

| 套餐 | 配置 | 流量 / 带宽 | 参考月付 | 购买 |
| --- | --- | --- | --- | --- |
| LAX.AS3.Pro.TINY | 1 核 / 2G / 20G SSD | 1000G @ 1Gbps | $10.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=253) |
| LAX.AS3.Pro.Pocket | 2 核 / 2G / 40G SSD | 1500G @ 4Gbps | $16.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=254) |
| LAX.AS3.Pro.STARTER | 2 核 / 2G / 80G SSD | 3000G @ 10Gbps | $34.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=255) |
| LAX.AS3.Pro.MINI | 4 核 / 4G / 80G SSD | 5000G @ 10Gbps | $62.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=256) |
| LAX.AS3.Pro.MICRO | 4 核 / 4G / 160G SSD | 7000G @ 10Gbps | $87.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=257) |
| LAX.AS3.Pro.MEDIUM | 6 核 / 8G / 160G SSD | 14000G @ 10Gbps | $199.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=258) |
| LAX.AN5.Pro.TINY | 1 核 / 2G / 20G SSD | 1000G @ 1Gbps | $14.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.Pocket | 2 核 / 2G / 40G SSD | 1500G @ 4Gbps | $21.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.STARTER | 2 核 / 2G / 80G SSD | 3000G @ 10Gbps | $43.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MINI | 4 核 / 4G / 80G SSD | 5000G @ 10Gbps | $79.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MICRO | 4 核 / 4G / 160G SSD | 7000G @ 10Gbps | $110.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MEDIUM | 6 核 / 8G / 160G SSD | 14000G @ 10Gbps | $289.90 | [ 选购 AN5 Pro](https://www.dmit.io/aff.php?aff=12046) |

AN5 平台往上还有 LARGE（8 核 / 16G / 320G，25T 流量）和 GIANT（12 核 / 24G / 640G，50T 流量），月付分别在 499.90 和 1009.90 美元档——这个价位已经属于企业业务范围了。

### 洛杉矶 LAX（Eyeball / 9929 + CMIN2）

| 套餐 | 配置 | 流量 / 带宽 | 参考月付 | 购买 |
| --- | --- | --- | --- | --- |
| LAX.AS3.EB.TINY | 1 核 / 2G / 20G SSD | 1500G @ 2Gbps | $10.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=259) |
| LAX.AS3.EB.Pocket | 2 核 / 2G / 40G SSD | 3000G @ 4Gbps | $16.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=260) |
| LAX.AS3.EB.STARTER | 2 核 / 2G / 80G SSD | 5000G @ 10Gbps | $34.90 | [ 查看该套餐](https://www.dmit.io/aff.php?aff=12046&pid=261) |
| LAX.AN5.EB.MINI | 4 核 / 4G / 80G SSD | 10000G @ 10Gbps | $79.90 | [ 选购 EB 套餐](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.EB.MICRO | 4 核 / 4G / 160G SSD | 14000G @ 10Gbps | $110.90 | [ 选购 EB 套餐](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.EB.MEDIUM | 6 核 / 8G / 160G SSD | 30000G @ 10Gbps | $289.90 | [ 选购 EB 套餐](https://www.dmit.io/aff.php?aff=12046) |

EB 和 Pro 在 AN5 平台上价格几乎一样，但流量给得更猛（同价位 EB.MINI 是 10T，Pro.MINI 是 5T），代价是回程走 9929 / CMIN2 而非 CN2 GIA。电信用户在这个档位上要多想想，移动联通用户基本可以放心选。

### 洛杉矶 LAX（Tier 1 / 国际线路）

T1 是 DMIT 里最便宜的一条线，也是价格最稳定的一条，多个第三方整理的价格基本一致。

| 套餐 | 配置 | 流量 / 带宽 | 参考价格 | 购买 |
| --- | --- | --- | --- | --- |
| LAX.T1.WEE | 1 核 / 1G / 20G SSD | 1000G @ 4Gbps | $36.90 / 年 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.TINY | 1 核 / 1G / 20G SSD | 2000G @ 4Gbps | $6.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.STARTER | 1 核 / 2G / 40G SSD | 4000G @ 10Gbps | $12.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.MINI | 2 核 / 2G / 60G SSD | 8000G @ 10Gbps | $21.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.MICRO | 4 核 / 4G / 80G SSD | 16000G @ 10Gbps | $32.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.MEDIUM | 4 核 / 8G / 160G SSD | 32000G @ 10Gbps | $49.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.LARGE | 8 核 / 16G / 320G SSD | 64000G @ 10Gbps | $99.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |
| LAX.T1.GIANT | 8 核 / 24G / 640G SSD | 128000G @ 10Gbps | $199.90 / 月 | [ 选购 T1](https://www.dmit.io/aff.php?aff=12046) |

AN5 平台上另有一条 T1 VOLUME 系列，规格命名变成 V2C2G、V2C4G 这种形式，2 核 2G / 40G / 5T 流量起步价 14.90 美元/月，往上到 4 核 8G / 160G / 40T 流量是 52.90 美元/月。它和经典 T1 档位的取舍点是流量额度和达量限速：VOLUME 走量大，达量后限速档位也更高。

### 香港 HKG

| 系列 / 套餐 | 配置 | 流量 / 带宽 | 参考价格 | 购买 |
| --- | --- | --- | --- | --- |
| HKG.Pro.TINY | 1 核 / 1G / 20G SSD | 500G @ 1Gbps | $39.90 / 月 | [ 选购香港 Pro](https://www.dmit.io/aff.php?aff=12046) |
| HKG.Pro.STARTER | 1 核 / 2G / 40G SSD | 1000G @ 1Gbps | $79.90 / 月 | [ 选购香港 Pro](https://www.dmit.io/aff.php?aff=12046) |
| HKG.Pro.MINI | 2 核 / 2G / 60G SSD | 1500G @ 1Gbps | $119.90 / 月 | [ 选购香港 Pro](https://www.dmit.io/aff.php?aff=12046) |
| HKG.Pro.MICRO | 4 核 / 4G / 80G SSD | 2000G @ 1Gbps | $159.90 / 月 | [ 选购香港 Pro](https://www.dmit.io/aff.php?aff=12046) |
| HKG.EB.MINIv2 | 2 核 / 2G / 60G SSD | 3000G @ 2Gbps | $89.90 / 月 | [ 选购香港 EB](https://www.dmit.io/aff.php?aff=12046) |
| HKG.EB.MICROv2 | 4 核 / 4G / 80G SSD | 4000G @ 4Gbps | $129.90 / 月 | [ 选购香港 EB](https://www.dmit.io/aff.php?aff=12046) |
| HKG.T1.WEE | 1 核 / 1G / 20G SSD | 1000G @ 1Gbps | $36.90 / 年 | [ 选购香港 T1](https://www.dmit.io/aff.php?aff=12046) |
| HKG.T1.TINY | 1 核 / 1G / 20G SSD | 2000G @ 4Gbps | $6.90 / 月 | [ 选购香港 T1](https://www.dmit.io/aff.php?aff=12046) |
| HKG.T1.MINI | 2 核 / 2G / 60G SSD | 8000G @ 10Gbps | $21.90 / 月 | [ 选购香港 T1](https://www.dmit.io/aff.php?aff=12046) |
| HKG.T1.MICRO | 4 核 / 4G / 80G SSD | 16000G @ 10Gbps | $32.90 / 月 | [ 选购香港 T1](https://www.dmit.io/aff.php?aff=12046) |

香港这条线还有个容易看漏的地方：原来叫 Lite 的大带宽产品已经改名叫 Standard，最低配的 6.90 美元款被取消了，现在月付 12.90 美元起。另外香港 Pro 常规产品已经整体升级到 AN5 平台（EPYC 9005 + DDR5）。至于 HKG.Pro 的限量特价机 Victoria（1 核 / 2G / 60G / 800G @ 500Mbps，年付约 298.88 美元），属于返场补货时才有货的款。

### 东京 TYO

| 系列 / 套餐 | 配置 | 流量 / 带宽 | 参考价格 | 购买 |
| --- | --- | --- | --- | --- |
| TYO.Pro.TINY | 1 核 / 1G / 20G SSD | 500G @ 1Gbps | $21.90 / 月 | [ 选购东京 Pro](https://www.dmit.io/aff.php?aff=12046) |
| TYO.Pro.MINI | 2 核 / 2G / 60G SSD | 2000G @ 1Gbps | $79.90 / 月 | [ 选购东京 Pro](https://www.dmit.io/aff.php?aff=12046) |
| TYO.Pro.MICRO | 4 核 / 4G / 80G SSD | 4000G @ 1Gbps | $159.90 / 月 | [ 选购东京 Pro](https://www.dmit.io/aff.php?aff=12046) |
| TYO.T1.WEE | 1 核 / 1G / 20G SSD | 1000G @ 1Gbps | $36.90 / 年 | [ 选购东京 T1](https://www.dmit.io/aff.php?aff=12046) |
| TYO.T1.MINI | 2 核 / 2G / 60G SSD | 8000G @ 10Gbps | $21.90 / 月 | [ 选购东京 T1](https://www.dmit.io/aff.php?aff=12046) |

东京的 Eyeball 系列已经按官方通知下线，现在只有 Pro 和 Tier 1 可选，还有返场性质的品川（Shinagawa）特价机，年付在 200 美元上下——不同批次开售的价格不太一样。

## 优惠和折扣：哪些能信，哪些已经作废

DMIT 没有长期有效的通用优惠码，日常折扣主要靠两种形式：

**一是年付折扣。** 年付通常比月付单价低，部分系列的最低配折扣力度更大。

**二是活动期的一次性码。** 黑五、圣诞这类节点，DMIT 会放出命名极长的活动码，比如「2025-XMAS-LAX-PRO-EB-ANNUALLY-STARTER-AND-HIGHER-15OFF-RECURRING」这种，从名字里就能读出适用范围：洛杉矶 Pro / EB、年付、STARTER 及以上、15% 循环折扣。这类码属于特定活动期的产物，现在再用基本都是无效的。

目前在多个来源里持续出现、可信度相对高的是 Standard（原 Lite）线的两个码：

> Lite-Annually-Recur-30OFF（年付 7 折）
> Lite-Semi-Annually-Recur-20OFF（半年付 8 折）

优惠码在结算页填进去点验证就能看到是否生效，不需要的话直接删掉即可。看到任何"永久 5 折""全系通用码"的说法，先去结算页验一下再信。

## 买之前必须搞清楚的六件事

这些政策比参数表更影响你的实际体验，尤其是前两条——很多人是踩过才知道。

**1. 退款政策**
新购服务 3 天内、流量使用不超过 30GB，可以申请全额退款；超过 3 天在 30 天内，可以按剩余价值退款。退款理由不要写成"线路不够好"或"IP 不是原生"这类主观原因，这是容易被驳回的点。退款一般在 48 小时内处理，促销期工单量大可能更慢。

**2. 换 IP 政策**
Pro 和 EB 系列满足条件可以免费换 IP：实例已使用满 7 天、距上次换 IP（含付费）至少 15 天、当前 IP 的 ICMP 和 TCP 端口全部被封、剩余有效期不少于 7 天。不满足条件的付费换 IP 是 5 美元一次，间隔不少于 7 天。如果 IP 在开通时就已经被封，可以直接开工单要求免费更换。

**3. 流量超了不会停机**
超出套餐流量额度后，机器不会被暂停，而是降到限速档继续不限量跑：Pro 和 EB 大概是 4~10Mbps，T1 系列按套餐在 100Mbps 到 500Mbps 之间。对偶尔超量的用户来说，这比直接断网友好不少。

**4. IP 质量不算稳定**
社区里的反馈比较一致：DMIT 的网络质量口碑好，但 IP 质量一般，有人拿到手就是墙的。下单时可以选择 IP Guarantee+ 选项，分配的 IP 在敏感地区不可用可以开工单免费重分配。买了准备长期用的话，这个选项值得勾。

**5. 风控和 Abuse 政策执行得很硬**
DMIT 对伪装域名、带 CDN 的站点这类安全问题会主动处理，流程是先关机、再要求整改、不整改就暂停服务。论坛里有用户反映收到过多次邮件通知、机器被关机的情况。合规用法没什么影响，但如果你打算用 CF 前置域名做伪装，得先知道这条线在哪里。

**6. 库存是个真问题**
热门特价机和 Pro / EB 的低配档经常缺货，补货基本是"上架即秒"。看中了别拖，但也别为了抢货买一个自己用不上的规格。

## 下单流程

官网下单不复杂：选机房 → 选线路档位 → 选套餐规格 → 选计费周期 → 在结算页填优惠码并验证 → 选择是否加 IP Guarantee+ → 支付宝或 PayPal 付款 → 自动开通。

一个实用建议：**第一次买先走月付。** 月付贵不了太多，但能让你在自己的宽带环境下把延迟、丢包和晚高峰表现验一遍。确认没问题再转年付拿折扣——DMIT 的续费和升级政策对老用户比较友好，按官网说法，升级产品或者改计费周期会按新的价格计算，但不主动变更的话已购产品价格不变。

## 常见问题

**DMIT 会超售吗？**
官方一直明确表示不超售，第三方对比内容里也把它作为和搬瓦工的主要差异之一。这个承诺没法从外部量化验证，但从它的定价策略看，靠超售走量不符合这家的路线。

**DMIT 和搬瓦工哪个好？**
两家都是三网优化线路的头部选择，DC1 机房的 CN2 上游其实就是 DMIT。差别在于：DMIT 硬件给得更高、支持免费换 IP（有条件）、出问题公告和补偿相对及时；搬瓦工在机房切换灵活性和产品成熟度上有优势。同线路水平下，DMIT 的价格通常更低一些。

**年付真的划算吗？**
单看单价是划算的，年付折扣叠加活动码能省下不小一笔。但前提是你已经确认这条线路适合自己。没验证过的线路直接上年付，退款政策只有 3 天全额这个窗口，风险要自己承担。

**香港贵那么多值不值？**
值不值取决于你的业务。面向国内用户的网站，香港 40ms 出头的延迟和洛杉矶 160ms 是两个量级的体验；但如果你只是自己用，晚高峰的实际感受差距没有价格差距那么大。洛杉矶 Pro 在大多数场景下已经够用。

**月付和季付会被区别对待吗？**
官方不保证月付周期分配的 IP 全球可用，这一点在买之前要清楚。需要稳定可用的 IP，就在下单时选 IP Guarantee+。

## 最后

DMIT 不是那种能"闭眼买"的便宜商家，它的价格摆在那里，且线路档次之间的差异需要你花点时间搞懂。但如果你想找一台面向大陆、晚高峰不用盯着监控看的机器，它在同价位里的选择并不多。

先想清楚自己是哪一类用户，再决定买哪条线、哪个机房，比看完一堆参数表直接下单要省事得多。
