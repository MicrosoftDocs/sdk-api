---
UID: NN:strmif.IAMDecoderCaps
title: IAMDecoderCaps (strmif.h)
description: The IAMDecoderCaps interface returns capabilities information from an MPEG decoder filter.
old-location: dshow\iamdecodercaps.htm
tech.root: DirectShow
ms.assetid: 3951200b-5a81-4832-9dae-021a76c1ab20
ms.date: 12/05/2018
ms.keywords: IAMDecoderCaps, IAMDecoderCaps interface [DirectShow], IAMDecoderCaps interface [DirectShow],described, IAMDecoderCapsInterface, dshow.iamdecodercaps, strmif/IAMDecoderCaps
f1_keywords:
- strmif/IAMDecoderCaps
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMDecoderCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDecoderCaps interface


## -description



The <code>IAMDecoderCaps</code> interface returns capabilities information from an MPEG decoder filter. The capabilities reported through this interface include whether the decoder supports the Video Mixing Renderer filter and whether it supports DirectX Video Acceleration.

Some DirectShow components, such as the DVD Graph Builder, use this interface to determine the correct filter graph to build. Applications might use this interface to query the decoder's capabilities.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDecoderCaps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDecoderCaps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDecoderCaps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdecodercaps-getdecodercaps">GetDecoderCaps</a>
</td>
<td align="left" width="63%">
Queries the decoder for its capabilities.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

