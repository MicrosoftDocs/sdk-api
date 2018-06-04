---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUserNotificationCallback interface


## -description


Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon. Used with <a href="https://msdn.microsoft.com/928e9a78-6976-4dcb-b01d-766561f6a861">IUserNotification2::Show</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserNotificationCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserNotificationCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserNotificationCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7360a2b-30ed-459e-ab6d-56a2127c2668">OnBalloonUserClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb0b1de0-a42c-4789-aac0-885a574f89f6">OnContextMenu</a>
</td>
<td align="left" width="63%">
Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0202aace-94d6-4619-8838-eea0b174ffb6">OnLeftClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.

</td>
</tr>
</table> 

