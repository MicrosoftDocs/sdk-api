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

# IEnhancedStorageSilo interface


## -description


The <b>IEnhancedStorageSilo</b> interface is the point of access for an IEEE 1667 silo and is used to obtain information and perform operations at the silo level.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageSilo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnhancedStorageSilo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnhancedStorageSilo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaf24814-b47a-4f33-ac17-d3b5b344f234">GetActions</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all actions available to the silo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98ef04a1-d14d-4de3-b24a-0f044335d75b">GetDevicePath</a>
</td>
<td align="left" width="63%">
Returns the path to the silo device node. The supplied string is suitable for passing to Windows System APIs such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff552074">SetupDiOpenDeviceInterface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Returns the general information associated with the silo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a95323d1-4329-4a1e-9c8a-adfdd199e9a5">GetPortableDevice</a>
</td>
<td align="left" width="63%">
Obtains an <a href="http://go.microsoft.com/fwlink/p/?linkid=134792">IPortableDevice</a> pointer used to issue  commands to the corresponding Enhanced Storage silo driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b52815e-e100-4c25-b7d3-8469d1dad745">SendCommand</a>
</td>
<td align="left" width="63%">
Sends a raw silo command to the silo object. This method is used to communicate with a silo which is not represented by a driver. 

</td>
</tr>
</table> 

