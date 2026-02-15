# 责任委托协议（RDP）

<p align="center">
  <strong>中文</strong> | <a href="README.md">English</a>
</p>

**协议名称：** 责任委托协议
**版本：** v0.1（概念草案）
**日期：** 2026年2月
**编辑：** HJS编辑

<p align="left">
  <a href="https://github.com/schchit/Responsibility-Delegation-Protocol">
    <img src="https://img.shields.io/badge/Status-Draft-blue" alt="Status">
  </a>
  <a href="https://creativecommons.org/licenses/by-sa/4.0/">
    <img src="https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey" alt="License">
  </a>
  <a href="https://github.com/schchit/Responsibility-Delegation-Protocol/issues">
    <img src="https://img.shields.io/badge/Issues-Welcome-brightgreen" alt="Issues">
  </a>
</p>

责任委托协议（RDP）是一个记录委托事实的协议层，与 HJS 核心协议共同使用。

## 概述

HJS 记录“谁执行了判断”。RDP 记录“谁有权执行此判断”以及“权从何来”。

权限系统回答“现在谁有权”。它们不回答权力从何而来、为何授予、持续多久、能否撤销。RDP 通过提供委托的证据层填补这一空白。

## 核心问题

**委托蒸发**：委托关系未被记录或无法验证，导致责任链断裂。

三类常见场景说明此问题：
- 通过非正式渠道的口头授权
- 授权链条无法追溯的转包关系
- 系统自动转移权限但未记录授权规则

在这些场景中，委托发生时没有正式记录，决策只检查当前权限，审计时无法追溯权力来源。

## 核心概念

| 术语 | 说明 |
|------|------|
| 责任委托 | 将特定范围内的决策权转移给另一主体 |
| 委托人 | 发起委托的主体 |
| 受托人 | 接受委托的主体 |
| 委托凭证 | 记录委托行为的数据结构 |
| 委托链 | 从原始责任主体到当前执行者的凭证序列 |

## 协议约束

- **不可绕过**：委托必须通过 RDP 完成
- **不可篡改存储**：凭证须写入不可篡改存储
- **无绕过路径**：不得提供不生成凭证的权限配置方式
- **双方确认**：委托须经委托人与受托人双方签名
- **明确范围**：须明确定义决策类型、阈值、有效期等
- **可撤销**：委托人可随时撤销委托
- **可审计**：委托链须完整可追溯

## 与 HJS 的关系
委托凭证 (RDP) → HJS 判断记录

text

RDP 可独立部署于任何需要记录委托关系的系统。

## 文档索引

- [English (full text)](responsibility-delegation-protocol-en.md)
- [中文（全文）](responsibility-delegation-protocol-zh-CN.md)

**版本：** v0.1（概念草案） · **许可证：** CC BY-SA 4.0
