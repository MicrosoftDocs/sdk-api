---
UID: NN:strmif.IAMOverlayFX
title: IAMOverlayFX (strmif.h)
description: The IAMOverlayFX interface controls how the video overlay appears on the user's screen. The Overlay Mixer filter implements this interface.helpviewer_keywords: ["IAMOverlayFX","IAMOverlayFX interface [DirectShow]","IAMOverlayFX interface [DirectShow]","described","IAMOverlayFXInterface","dshow.iamoverlayfx","strmif/IAMOverlayFX"]
old-location: dshow\iamoverlayfx.htm
tech.root: DirectShow
ms.assetid: 6bc78464-8c9e-4016-b9aa-6589d53d45bf
ms.date: 12/05/2018
ms.keywords: IAMOverlayFX, IAMOverlayFX interface [DirectShow], IAMOverlayFX interface [DirectShow],described, IAMOverlayFXInterface, dshow.iamoverlayfx, strmif/IAMOverlayFX
f1_keywords:
- strmif/IAMOverlayFX
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
- IAMOverlayFX
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMOverlayFX interface


## -description



The <code>IAMOverlayFX</code> interface controls how the video overlay appears on the user's screen. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMOverlayFX</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMOverlayFX</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMOverlayFX</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-getoverlayfx">GetOverlayFX</a>
</td>
<td align="left" width="63%">
Retrieves the effects currently applied to the overlay surface, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-queryoverlayfxcaps">QueryOverlayFXCaps</a>
</td>
<td align="left" width="63%">
Retrieves information about which overlay effects are available to the Overlay Mixer filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-setoverlayfx">SetOverlayFX</a>
</td>
<td align="left" width="63%">
Applies the specified effects to the overlay surface.

</td>
</tr>
</table> 

