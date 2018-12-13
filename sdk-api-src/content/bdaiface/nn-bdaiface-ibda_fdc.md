---
UID: NN:bdaiface.IBDA_FDC
title: IBDA_FDC
author: windows-sdk-content
description: Provides access to a device's Forward Data Channel (FDC) Service. The FDC is an out-of-band channel that carries configuration and control messages.
old-location: mstv\ibda_fdc.htm
tech.root: mstv
ms.assetid: 8b7a07fd-99e9-4f8e-9211-109689f2f892
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_FDC, IBDA_FDC interface [Microsoft TV Technologies], IBDA_FDC interface [Microsoft TV Technologies],described, bdaiface/IBDA_FDC, mstv.ibda_fdc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_FDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693348(v=VS.85).aspx">AddPid</a>
</td>
<td align="left" width="63%">
Adds one or more packet identifiers (PIDs) to the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693349(v=VS.85).aspx">AddTid</a>
</td>
<td align="left" width="63%">
Adds one or more table identifiers (TIDs) to the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693350(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the tuning status of the FDC stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693351(v=VS.85).aspx">GetTableSection</a>
</td>
<td align="left" width="63%">
Gets the latest table section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693352(v=VS.85).aspx">RemovePid</a>
</td>
<td align="left" width="63%">
Removes one or more PIDs from the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693353(v=VS.85).aspx">RemoveTid</a>
</td>
<td align="left" width="63%">
Removes one or more TIDs from the MPEG flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693354(v=VS.85).aspx">RequestTables</a>
</td>
<td align="left" width="63%">
Requests MPEG-2 table sections, filtered by TID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_FDC)</code>.



