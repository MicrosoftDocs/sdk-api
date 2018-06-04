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

# IUPnPNAT interface


## -description


The 
<b>IUPnPNAT</b> interface is the primary interface for managing Network Address Translation (NAT) with UPnP. The 
<b>IUPnPNAT</b> interface provides access directly or indirectly to all the other interfaces in the NAT API with UPnP technology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPNAT</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUPnPNAT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPNAT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DynamicPortMappingCollection</b></td>
<td align="left" width="63%">
This method is not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/594fdd40-062e-4f81-af11-4170a5870472">get_NATEventManager</a>
</td>
<td align="left" width="63%">
Establishes callbacks for the NAT to inform the client of changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba4d0735-f04e-47d1-a54c-e01cf338d737">get_StaticPortMappingCollection</a>
</td>
<td align="left" width="63%">
Retrieves the static port mappings collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>
 

 

