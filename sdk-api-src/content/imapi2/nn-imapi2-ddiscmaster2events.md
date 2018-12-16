---
UID: NN:imapi2.DDiscMaster2Events
title: DDiscMaster2Events
author: windows-sdk-content
description: Implement this interface to receive notification when a CD or DVD device is added to or removed from the computer.
old-location: imapi\ddiscmaster2events.htm
tech.root: imapi
ms.assetid: f01fa2d8-989d-499f-b79d-495108640aa2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DDiscMaster2Events, DDiscMaster2Events interface [IMAPI], DDiscMaster2Events interface [IMAPI],described, imapi.ddiscmaster2events, imapi2/DDiscMaster2Events
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscMaster2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DDiscMaster2Events interface


## -description


Implement this interface to receive notification when a CD or DVD device is added to or removed from the computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DDiscMaster2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>DDiscMaster2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DDiscMaster2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f728b33-3788-4fc4-b261-da243b4ff46e">NotifyDeviceAdded</a>
</td>
<td align="left" width="63%">
Receives notification when an optical media device is added to the computer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/626096ba-f2d7-4a75-b04c-f95aad6915cc">NotifyDeviceRemoved</a>
</td>
<td align="left" width="63%">
Receives notification when an optical media device is removed from the computer. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>
 

 

