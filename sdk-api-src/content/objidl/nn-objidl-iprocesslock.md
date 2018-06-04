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

# IProcessLock interface


## -description


<p class="CCE_Message">[The use of this interface is not recommended; use the <a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a> interface instead.]

Used by <a href="https://msdn.microsoft.com/01773aa6-3eb5-43dd-8a10-d1351a07fe1f">ISurrogateService</a> to prevent the process from terminating due to a time-out.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProcessLock</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IProcessLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProcessLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c82273f-7303-45c2-92e2-48ffab094756">AddRefOnProcess</a>
</td>
<td align="left" width="63%">
Increments the reference count of the process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0943afc-b20f-4082-b561-552370a630a1">ReleaseRefOnProcess</a>
</td>
<td align="left" width="63%">
Decrements the reference count of the process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a>
 

 

