---
UID: NN:d2d1_3.ID2D1ImageSourceFromWic
title: ID2D1ImageSourceFromWic (d2d1_3.h)
description: Produces 2D pixel data that has been sourced from WIC.helpviewer_keywords: ["ID2D1ImageSourceFromWic","ID2D1ImageSourceFromWic interface [Direct2D]","ID2D1ImageSourceFromWic interface [Direct2D]","described","d2d1_3/ID2D1ImageSourceFromWic","direct2d.id2d1imagesourcefromwic"]
old-location: direct2d\id2d1imagesourcefromwic.htm
tech.root: Direct2D
ms.assetid: EA1F1377-A314-4375-AB86-A36CFE5AF0C8
ms.date: 12/05/2018
ms.keywords: ID2D1ImageSourceFromWic, ID2D1ImageSourceFromWic interface [Direct2D], ID2D1ImageSourceFromWic interface [Direct2D],described, d2d1_3/ID2D1ImageSourceFromWic, direct2d.id2d1imagesourcefromwic
f1_keywords:
- d2d1_3/ID2D1ImageSourceFromWic
dev_langs:
- c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d2d1_3.dll
api_name:
- ID2D1ImageSourceFromWic
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1ImageSourceFromWic interface


## -description


Produces 2D pixel data that has been sourced from WIC.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ImageSourceFromWic</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesource">ID2D1ImageSource</a>. <b>ID2D1ImageSourceFromWic</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ImageSourceFromWic</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-ensurecached">EnsureCached</a>
</td>
<td align="left" width="63%">Overloaded. Loads image data into caches of image sources if that data is not already cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1imagesourcefromwic-getsource">GetSource</a>
</td>
<td align="left" width="63%">
Retrieves the underlying bitmap image source from the Windows Imaging Component (WIC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-trimcache">TrimCache</a>
</td>
<td align="left" width="63%">Overloaded. Trims the populated regions of the image source cache to just the specified rectangle.

</td>
</tr>
</table> 


## -remarks



Create an an instance of ID2D1ImageSourceFromWic 
          using [ID2D1DeviceContext2::CreateImageSourceFromWic](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))a>.
        



