﻿---
title: '變更預設離線通訊錄: Exchange Online Help'
TOCTitle: 變更預設離線通訊錄
ms:assetid: 61abf78e-2543-4431-acc8-839e3c7a4548
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Aa998569(v=EXCHG.150)
ms:contentKeyID: 50473326
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 變更預設離線通訊錄

 

_**適用版本：**Exchange Online, Exchange Server 2013_

_**上次修改主題的時間：**2014-12-16_

根據預設，當您安裝信箱伺服器角色會建立名為預設離線通訊錄 Web 式預設離線通訊錄 (OAB)。您可以為預設 OAB Exchange組織中設定任何 OAB。這個新的預設 OAB 相關聯的所有新建立的信箱資料庫。您可以在組織中有一個預設 OAB。如果您刪除預設 OAB， MicrosoftExchange不會自動指派給另一個 OAB 為預設值。您必須手動指定另一個 OAB 為預設值。

如需與 OAB 相關的其他管理工作，請參閱[離線通訊錄程序](offline-address-book-procedures-exchange-2013-help.md)。

## 開始之前有哪些須知？

  - 每項程序的預估完成時間：5 分鐘。

  - 您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [收件者權限](recipients-permissions-exchange-2013-help.md)主題中的「離線通訊錄」項目。

  - 根據 Exchange Online 的預設，「通訊清單」角色並未指派給任何角色群組。若要使用任何需要「通訊清單」角色的指令程式，您需將此角色新增至角色群組。如需詳細資訊，請參閱＜[管理角色群組](manage-role-groups-exchange-2013-help.md)＞主題的＜將角色新增至角色群組＞一節。

  - 您無法使用 Exchange 系統管理中心 (EAC) 執行此程序。您必須使用命令介面。

  - 如需適用於此主題中程序的快速鍵相關資訊，請參閱 [Exchange 系統管理中心的鍵盤快速鍵](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.tip(EXCHG.150).gif" title="提示" alt="提示" />提示：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>有問題嗎？在 Exchange 論壇中尋求協助。 論壇的網址為：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。</td>
</tr>
</tbody>
</table>


## 使用命令介面變更預設 OAB

此範例會將名為 My OAB 的 OAB 設定為預設 OAB。

    Set-OfflineAddressBook -Identity "My OAB" -IsDefault $true

如需詳細的語法及參數資訊，請參閱 [Set-OfflineAddressBook](https://technet.microsoft.com/zh-tw/library/aa996330\(v=exchg.150\))。

