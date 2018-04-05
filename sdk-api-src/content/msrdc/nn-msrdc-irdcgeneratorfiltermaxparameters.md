---
UID: NN:msrdc.IRdcGeneratorFilterMaxParameters
title: IRdcGeneratorFilterMaxParameters
author: windows-driver-content
description: Sets and retrieves parameters used by the FilterMax generator.
old-location: rdc\irdcgeneratorfiltermaxparameters.htm
old-project: Rdc
ms.assetid: 6767ab24-2bb6-48bf-8f12-794d8b22e2b7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRdcGeneratorFilterMaxParameters, IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression], IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression], described, fs.irdcgeneratorfiltermaxparameters, msrdc/IRdcGeneratorFilterMaxParameters, rdc.irdcgeneratorfiltermaxparameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcGeneratorFilterMaxParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

