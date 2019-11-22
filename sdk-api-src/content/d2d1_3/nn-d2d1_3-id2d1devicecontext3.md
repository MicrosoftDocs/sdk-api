---
UID: NN:d2d1_3.ID2D1DeviceContext3
title: ID2D1DeviceContext3 (d2d1_3.h)

description: This interface performs all the same functions as the ID2D1DeviceContext2 interface, plus it enables functionality for creating and drawing sprite batches.
old-location: direct2d\id2d1devicecontext3.htm
tech.root: Direct2D
ms.assetid: AD763619-7880-41EB-8446-2E4B84CB4EAC

ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext3, ID2D1DeviceContext3 interface [Direct2D], ID2D1DeviceContext3 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext3, direct2d.id2d1devicecontext3
ms.topic: interface
f1_keywords: 
 - "d2d1_3/ID2D1DeviceContext3"
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
req.lib: D2d1.lib
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
 - ID2D1DeviceContext3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext3 interface


## -description


This interface performs all the same functions as the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a> interface, plus it enables functionality for creating and drawing sprite batches.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>. <b>ID2D1DeviceContext3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch">CreateSpriteBatch</a>
</td>
<td align="left" width="63%">
Creates a new, empty sprite batch. After creating a sprite batch, use <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-addsprites">ID2D1SpriteBatch::AddSprites</a> 
        to add sprites to it, then use <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-drawspritebatch">ID2D1DeviceContext3::DrawSpriteBatch</a> to draw it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-drawspritebatch">DrawSpriteBatch</a>
</td>
<td align="left" width="63%">Overloaded. Renders part or all of the given sprite batch to the device context using the specified drawing options.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
 

 

