---
UID: NN:d2d1_3.ID2D1SpriteBatch
title: ID2D1SpriteBatch (d2d1_3.h)
author: windows-sdk-content
description: Represents a single group of sprites with their associated drawing properties.
old-location: direct2d\id2d1spritebatch.htm
tech.root: Direct2D
ms.assetid: D33958D5-D31C-47DC-B172-CADB1F1B81AE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SpriteBatch, ID2D1SpriteBatch interface [Direct2D], ID2D1SpriteBatch interface [Direct2D],described, d2d1_3/ID2D1SpriteBatch, direct2d.id2d1spritebatch
ms.topic: interface
f1_keywords: 
 - "d2d1_3/ID2D1SpriteBatch"
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
 - ID2D1SpriteBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SpriteBatch interface


## -description


Represents a single group of sprites with their associated drawing properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SpriteBatch</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1SpriteBatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SpriteBatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-addsprites">AddSprites</a>
</td>
<td align="left" width="63%">
Adds the given sprites to the end of this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all sprites from this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-getspritecount">GetSpriteCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of sprites in this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-getsprites">GetSprites</a>
</td>
<td align="left" width="63%">
Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-setsprites">SetSprites</a>
</td>
<td align="left" width="63%">
Updates the properties of the specified sprites in this sprite batch.

</td>
</tr>
</table> 


## -remarks



Create a new sprite batch using <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch">ID2D1DeviceContext3::CreateSpriteBatch</a>. 
          Use <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-addsprites">ID2D1SpriteBatch::AddSprites</a>to add sprites to the batch, then use <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-drawspritebatch">ID2D1DeviceContext3::DrawSpriteBatch</a> to draw them.
        

Sprites are a way for apps to draw a large number of images very efficiently. 
        They are commonly used to render characters and backgrounds in 2D games, or to render particle systems such as smoke and flames. 
        If your app has performance demands and needs to draw hundreds or thousands of images every frame, then consider taking advantage of sprite batches and the fine-grained control they offer, 
        instead of the general-purpose DrawImage method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>
 

 

