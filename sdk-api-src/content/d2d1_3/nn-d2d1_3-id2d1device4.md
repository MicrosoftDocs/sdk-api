---
UID: NN:d2d1_3.ID2D1Device4
title: ID2D1Device4 (d2d1_3.h)
description: Represents a resource domain whose objects and device contexts can be used together. This interface performs all the same functions as the ID2D1Device3 interface. It also enables the creation of ID2D1DeviceContext4 objects.helpviewer_keywords: ["ID2D1Device4","ID2D1Device4 interface [Direct2D]","ID2D1Device4 interface [Direct2D]","described","d2d1_3/ID2D1Device4","direct2d.id2d1device4"]
old-location: direct2d\id2d1device4.htm
tech.root: Direct2D
ms.assetid: B91E4E63-5FB5-4470-A3B9-F94008EAE4E9
ms.date: 12/05/2018
ms.keywords: ID2D1Device4, ID2D1Device4 interface [Direct2D], ID2D1Device4 interface [Direct2D],described, d2d1_3/ID2D1Device4, direct2d.id2d1device4
f1_keywords:
- d2d1_3/ID2D1Device4
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Device4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Device4 interface


## -description


Represents a resource domain whose objects and device contexts can be used together.
          This interface performs all the same functions as the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a> interface.
          It also enables the creation of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a> objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a>. <b>ID2D1Device4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1device4-createdevicecontext">CreateDeviceContext</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a> from this Direct2D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1device4-getmaximumcolorglyphcachememory">GetMaximumColorGlyphCacheMemory</a>
</td>
<td align="left" width="63%">
Gets the maximum capacity of the color glyph cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1device4-setmaximumcolorglyphcachememory">SetMaximumColorGlyphCacheMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum capacity of the color glyph cache. 

</td>
</tr>
</table> 

