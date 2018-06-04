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

# INetFwServiceRestriction interface


## -description


The <b>INetFwServiceRestriction</b> interface provides access to the Windows Service Hardening networking rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServiceRestriction</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetFwServiceRestriction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwServiceRestriction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12846607-daf7-43ce-8278-89db15b95a81">get_Rules</a>
</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5695bcb7-a83a-4581-8f46-00e85273b160">RestrictService</a>
</td>
<td align="left" width="63%">
Turns service restriction on or off for a given service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38fe5a68-44ab-4bcb-8673-ebb1e87e446f">ServiceRestricted</a>
</td>
<td align="left" width="63%">
Queries the service restriction state of a given service.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServiceRestriction</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/12846607-daf7-43ce-8278-89db15b95a81">Rules</a>


</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules

</td>
</tr>
</table> 


## -remarks



When adding rules, note that there may be a small time lag before the newly-added rule is applied.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="_com_iunknown">IUnknown</a>
 

 

