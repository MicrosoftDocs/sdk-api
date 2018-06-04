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

# IBDA_FDC interface


## -description


Provides access to a device's Forward Data Channel (FDC) Service. The FDC is an out-of-band channel that carries configuration and control messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_FDC</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_FDC</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_FDC</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28bc019c-1b5e-43e2-9fb4-7274d9c0e275">AddPid</a>
</td>
<td align="left" width="63%">
Adds one or more packet identifiers (PIDs) to the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cd39bbc-106b-4411-bc42-a1adc360e121">AddTid</a>
</td>
<td align="left" width="63%">
Adds one or more table identifiers (TIDs) to the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the tuning status of the FDC stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c83234-c752-4f94-a3f1-cc62a5da894a">GetTableSection</a>
</td>
<td align="left" width="63%">
Gets the latest table section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1277726c-6443-416c-a5d4-044d5f885af7">RemovePid</a>
</td>
<td align="left" width="63%">
Removes one or more PIDs from the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fac8f486-e24e-4996-a90f-f8947d43d209">RemoveTid</a>
</td>
<td align="left" width="63%">
Removes one or more TIDs from the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8483d3-6c4c-4786-a99b-bf3575a18fdb">RequestTables</a>
</td>
<td align="left" width="63%">
Requests MPEG-2 table sections, filtered by TID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_FDC)</code>.



