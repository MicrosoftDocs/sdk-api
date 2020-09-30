---
UID: NN:dwrite.IDWritePixelSnapping
title: IDWritePixelSnapping (dwrite.h)
description: Defines the pixel snapping properties such as pixels per DIP(device-independent pixel) and the current transform matrix of a text renderer.
helpviewer_keywords: ["IDWritePixelSnapping","IDWritePixelSnapping interface [Direct Write]","IDWritePixelSnapping interface [Direct Write]","described","directwrite.IDWritePixelSnapping","dwrite/IDWritePixelSnapping"]
old-location: directwrite\IDWritePixelSnapping.htm
tech.root: DirectWrite
ms.assetid: b1b1eeb7-934f-42f4-ac01-50973a94996e
ms.date: 12/05/2018
ms.keywords: IDWritePixelSnapping, IDWritePixelSnapping interface [Direct Write], IDWritePixelSnapping interface [Direct Write],described, directwrite.IDWritePixelSnapping, dwrite/IDWritePixelSnapping
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWritePixelSnapping
 - dwrite/IDWritePixelSnapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWritePixelSnapping
---

# IDWritePixelSnapping interface


## -description

Defines the pixel snapping properties such as pixels per DIP(device-independent pixel) and the current transform matrix of a text renderer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWritePixelSnapping</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWritePixelSnapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWritePixelSnapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritepixelsnapping-getcurrenttransform">GetCurrentTransform</a>
</td>
<td align="left" width="63%">
 Gets a transform that maps abstract coordinates to DIPs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritepixelsnapping-getpixelsperdip">GetPixelsPerDip</a>
</td>
<td align="left" width="63%">
 Gets the number of physical pixels per DIP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/win32/legacy/dd371281(v=vs.85)">IsPixelSnappingDisabled</a>
</td>
<td align="left" width="63%">
 Determines whether pixel snapping is disabled. The recommended default is <b>FALSE</b>, unless doing animation that requires subpixel vertical placement.

</td>
</tr>
</table>