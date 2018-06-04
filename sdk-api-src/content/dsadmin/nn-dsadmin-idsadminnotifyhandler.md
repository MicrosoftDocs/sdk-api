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

# IDsAdminNotifyHandler interface


## -description


The <b>IDsAdminNotifyHandler</b> interface is implemented by an Active Directory administrative notification handler. This interface is used by the Active Directory Users and Computers MMC snap-in to notify registered handlers when certain events, such as deleting or renaming an object, occur. The snap-in creates an instance of this object by calling <a href="_com_cocreateinstance">CoCreateInstance</a> with the CLSID of the extension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNotifyHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsAdminNotifyHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsAdminNotifyHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">Begin</a>
</td>
<td align="left" width="63%">
Called when an event, that the notification handler has requested, occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ff92b54-fa2c-4f45-8f40-e9c884e9cf7e">End</a>
</td>
<td align="left" width="63%">
Called after the notification event has occurred. This method is called even if the notification process is canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Called to initialize the  notification  handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">Notify</a>
</td>
<td align="left" width="63%">
Called once for each object after the confirmation dialog box has been displayed and the notification handler was selected in the confirmation dialog box.

</td>
</tr>
</table> 


## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>
 

 

