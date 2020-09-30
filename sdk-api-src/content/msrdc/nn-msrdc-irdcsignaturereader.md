---
UID: NN:msrdc.IRdcSignatureReader
title: IRdcSignatureReader (msrdc.h)
description: Reads the signatures and the parameters used to generate the signatures.
helpviewer_keywords: ["IRdcSignatureReader","IRdcSignatureReader interface [Remote Differential Compression]","IRdcSignatureReader interface [Remote Differential Compression]","described","fs.irdcsignaturereader","msrdc/IRdcSignatureReader","rdc.irdcsignaturereader"]
old-location: rdc\irdcsignaturereader.htm
tech.root: rdc
ms.assetid: dec6eb10-1243-4888-9ccc-ab1f4cfb11e7
ms.date: 12/05/2018
ms.keywords: IRdcSignatureReader, IRdcSignatureReader interface [Remote Differential Compression], IRdcSignatureReader interface [Remote Differential Compression],described, fs.irdcsignaturereader, msrdc/IRdcSignatureReader, rdc.irdcsignaturereader
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
 - IRdcSignatureReader
 - msrdc/IRdcSignatureReader
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
 - IRdcSignatureReader
---

# IRdcSignatureReader interface


## -description

The <b>IRdcSignatureReader</b> interface reads the signatures and the parameters used to generate the signatures.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcSignatureReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcSignatureReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcSignatureReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsignaturereader-readheader">ReadHeader</a>
</td>
<td align="left" width="63%">
Reads the signature header and returns a copy of the parameters
   used to generate the signatures.</p> (Inherited from <b>IRdcSignatureReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsignaturereader-readsignatures">ReadSignatures</a>
</td>
<td align="left" width="63%">
Reads a block of signatures from the current position.</p> (Inherited from <b>IRdcSignatureReader</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>