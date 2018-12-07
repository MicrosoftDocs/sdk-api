---
UID: NN:dsadmin.IDsAdminNotifyHandler
title: IDsAdminNotifyHandler
author: windows-sdk-content
description: The IDsAdminNotifyHandler interface is implemented by an Active Directory administrative notification handler.
old-location: ad\idsadminnotifyhandler.htm
tech.root: ad
ms.assetid: d55e1473-8e51-441e-bd22-63208b294e14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDsAdminNotifyHandler, IDsAdminNotifyHandler interface [Active Directory], IDsAdminNotifyHandler interface [Active Directory],described, _glines_idsadminnotifyhandler, ad.idsadminnotifyhandler, dsadmin/IDsAdminNotifyHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dsadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNotifyHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNotifyHandler interface


## -description


The <b>IDsAdminNotifyHandler</b> interface is implemented by an Active Directory administrative notification handler. This interface is used by the Active Directory Users and Computers MMC snap-in to notify registered handlers when certain events, such as deleting or renaming an object, occur. The snap-in creates an instance of this object by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with the CLSID of the extension.


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
<a href="https://msdn.microsoft.com/7fcd49d3-ccdb-4d55-96ea-cc925a36c366">Initialize</a>
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




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>
 

 

