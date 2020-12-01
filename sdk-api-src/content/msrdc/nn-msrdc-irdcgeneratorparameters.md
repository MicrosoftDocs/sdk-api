---
UID: NN:msrdc.IRdcGeneratorParameters
title: IRdcGeneratorParameters (msrdc.h)
description: Is the generic interface for all types of generator parameters. All generator parameter objects must support this interface.
helpviewer_keywords: ["IRdcGeneratorParameters","IRdcGeneratorParameters interface [Remote Differential Compression]","IRdcGeneratorParameters interface [Remote Differential Compression]","described","fs.irdcgeneratorparameters","msrdc/IRdcGeneratorParameters","rdc.irdcgeneratorparameters"]
old-location: rdc\irdcgeneratorparameters.htm
tech.root: rdc
ms.assetid: 1b2db5c5-79eb-490a-ae03-36b0e926725d
ms.date: 12/05/2018
ms.keywords: IRdcGeneratorParameters, IRdcGeneratorParameters interface [Remote Differential Compression], IRdcGeneratorParameters interface [Remote Differential Compression],described, fs.irdcgeneratorparameters, msrdc/IRdcGeneratorParameters, rdc.irdcgeneratorparameters
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
 - IRdcGeneratorParameters
 - msrdc/IRdcGeneratorParameters
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
 - IRdcGeneratorParameters
---

# IRdcGeneratorParameters interface


## -description

The <b>IRdcGeneratorParameters</b> interface 
    is the generic interface for all types of generator parameters. All generator parameter objects must 
    support this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGeneratorParameters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcGeneratorParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcGeneratorParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-getgeneratorparameterstype">GetGeneratorParametersType</a>
</td>
<td align="left" width="63%">
Returns the specific type of the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-getparametersversion">GetParametersVersion</a>
</td>
<td align="left" width="63%">
Returns information about the version of RDC used to serialize the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-getserializesize">GetSerializeSize</a>
</td>
<td align="left" width="63%">
Returns the size, in bytes, of the serialized parameter data.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the parameter data into a block of memory.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>