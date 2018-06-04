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

# IRdcGeneratorFilterMaxParameters interface


## -description


The <b>IRdcGeneratorFilterMaxParameters</b> 
    interface sets and retrieves parameters used by the FilterMax generator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGeneratorFilterMaxParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcGeneratorFilterMaxParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcGeneratorFilterMaxParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a0460c-ca48-48ca-bd5b-1213e8279366">GetHashWindowSize</a>
</td>
<td align="left" width="63%">
Returns the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6509330a-9592-4e10-91fb-43e4b63dceb9">GetHorizonSize</a>
</td>
<td align="left" width="63%">
Returns the horizon size—the length over which the FilterMax generator looks 
    for local maxima.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b18a5db1-f480-46c4-bac3-b0b2f0da6cfa">SetHashWindowSize</a>
</td>
<td align="left" width="63%">
Sets the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/becd1edd-d06d-4328-8a7a-678f893bad3a">SetHorizonSize</a>
</td>
<td align="left" width="63%">
Sets the horizon size—the length over which the FilterMax generator looks 
    for local maxima.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 

