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

# IBDA_NetworkProvider interface


## -description



The <b>IBDA_NetworkProvider</b> interface is implemented on a Network Provider filter. It provides methods that BDA device filters call to register themselves after they are added to the graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_NetworkProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_NetworkProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_NetworkProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38d9f099-b639-41fe-b0fd-82f056622de0">GetNetworkType</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/943b3c1f-4aea-4c16-b730-74b63397ad9f">GetSignalSource</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c7305a1-4a63-42a9-abc2-ae5394c3be9a">GetTuningSpace</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e461ff83-c3fc-43f2-934b-3f4c3afd0061">PutSignalSource</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to specify the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4541a675-875b-4a6c-8251-e13abdd46b38">PutTuningSpace</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to specify the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88050024-5960-4ce5-8645-82db3e17b12c">RegisterDeviceFilter</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to register itself in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d54830f-93cc-44c0-9bb7-43c439f4aa8e">UnRegisterDeviceFilter</a>
</td>
<td align="left" width="63%">
Called by BDA device filters when they are removed from the filter graph.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NetworkProvider)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

