---
UID: NN:msrdc.IRdcGeneratorFilterMaxParameters
title: IRdcGeneratorFilterMaxParameters (msrdc.h)
description: Sets and retrieves parameters used by the FilterMax generator.
helpviewer_keywords: ["IRdcGeneratorFilterMaxParameters","IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression]","IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression]","described","fs.irdcgeneratorfiltermaxparameters","msrdc/IRdcGeneratorFilterMaxParameters","rdc.irdcgeneratorfiltermaxparameters"]
old-location: rdc\irdcgeneratorfiltermaxparameters.htm
tech.root: rdc
ms.assetid: 6767ab24-2bb6-48bf-8f12-794d8b22e2b7
ms.date: 12/05/2018
ms.keywords: IRdcGeneratorFilterMaxParameters, IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression], IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],described, fs.irdcgeneratorfiltermaxparameters, msrdc/IRdcGeneratorFilterMaxParameters, rdc.irdcgeneratorfiltermaxparameters
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcGeneratorFilterMaxParameters
 - msrdc/IRdcGeneratorFilterMaxParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGeneratorFilterMaxParameters
---

# IRdcGeneratorFilterMaxParameters interface


## -description

The <b>IRdcGeneratorFilterMaxParameters</b> 
    interface sets and retrieves parameters used by the FilterMax generator.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGeneratorFilterMaxParameters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcGeneratorFilterMaxParameters</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-gethashwindowsize">GetHashWindowSize</a>
</td>
<td align="left" width="63%">
Returns the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-gethorizonsize">GetHorizonSize</a>
</td>
<td align="left" width="63%">
Returns the horizon size—the length over which the FilterMax generator looks 
    for local maxima.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-sethashwindowsize">SetHashWindowSize</a>
</td>
<td align="left" width="63%">
Sets the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-sethorizonsize">SetHorizonSize</a>
</td>
<td align="left" width="63%">
Sets the horizon size—the length over which the FilterMax generator looks 
    for local maxima.</p> (Inherited from <b>IRdcGeneratorFilterMaxParameters</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>