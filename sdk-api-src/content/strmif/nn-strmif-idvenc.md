---
UID: NN:strmif.IDVEnc
title: IDVEnc (strmif.h)
description: The IDVEnc interface sets and retrieves properties on the DV Video Encoder filter.
helpviewer_keywords: ["IDVEnc","IDVEnc interface [DirectShow]","IDVEnc interface [DirectShow]","described","IDVEncInterface","dshow.idvenc","strmif/IDVEnc"]
old-location: dshow\idvenc.htm
tech.root: dshow
ms.assetid: f193b76f-ca6a-44f5-b097-1570c4527ab4
ms.date: 12/05/2018
ms.keywords: IDVEnc, IDVEnc interface [DirectShow], IDVEnc interface [DirectShow],described, IDVEncInterface, dshow.idvenc, strmif/IDVEnc
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDVEnc
 - strmif/IDVEnc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDVEnc
---

# IDVEnc interface


## -description

The <code>IDVEnc</code> interface sets and retrieves properties on the <a href="/windows/desktop/DirectShow/dv-video-encoder-filter">DV Video Encoder</a> filter.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVEnc</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVEnc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVEnc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-idvenc-get_iformatresolution">get_IFormatResolution</a>
</td>
<td align="left" width="63%">
Retrieves the encoding resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-idvenc-put_iformatresolution">put_IFormatResolution</a>
</td>
<td align="left" width="63%">
Sets the encoding resolution.

</td>
</tr>
</table>