---
UID: NN:d2d1_3.ID2D1SpriteBatch
title: ID2D1SpriteBatch
author: windows-sdk-content
description: Represents a single group of sprites with their associated drawing properties.
old-location: direct2d\id2d1spritebatch.htm
tech.root: direct2d
ms.assetid: D33958D5-D31C-47DC-B172-CADB1F1B81AE
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ID2D1SpriteBatch, ID2D1SpriteBatch interface [Direct2D], ID2D1SpriteBatch interface [Direct2D],described, d2d1_3/ID2D1SpriteBatch, direct2d.id2d1spritebatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ID2D1SpriteBatch interface


## -description


Represents a single group of sprites with their associated drawing properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SpriteBatch</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1SpriteBatch</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/49EA1F42-76C3-4505-B46A-422A336A13F6">AddSprites</a>
</td>
<td align="left" width="63%">
Adds the given sprites to the end of this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01CCF4B6-C3CA-4E59-8436-AAE633C7A5FD">Clear</a>
</td>
<td align="left" width="63%">
Removes all sprites from this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4116A067-A02D-414F-B7A4-7D0B6A42653A">GetSpriteCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of sprites in this sprite batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39B6D8ED-25B2-4542-8994-FD607E60E19A">GetSprites</a>
</td>
<td align="left" width="63%">
Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6BC5740F-520D-47EA-A90A-973E158F2AC2">SetSprites</a>
</td>
<td align="left" width="63%">
Updates the properties of the specified sprites in this sprite batch.

</td>
</tr>
</table> 


## -remarks



Create a new sprite batch using <a href="https://msdn.microsoft.com/C9CCDF6B-BAEC-4C37-B3C1-60D50BACF973">ID2D1DeviceContext3::CreateSpriteBatch</a>. 
          Use <a href="https://msdn.microsoft.com/49EA1F42-76C3-4505-B46A-422A336A13F6">ID2D1SpriteBatch::AddSprites</a>to add sprites to the batch, then use <a href="https://msdn.microsoft.com/66d049ca-5d4b-1570-3fa3-8991f9fc97a0">ID2D1DeviceContext3::DrawSpriteBatch</a> to draw them.
        

Sprites are a way for apps to draw a large number of images very efficiently. 
        They are commonly used to render characters and backgrounds in 2D games, or to render particle systems such as smoke and flames. 
        If your app has performance demands and needs to draw hundreds or thousands of images every frame, then consider taking advantage of sprite batches and the fine-grained control they offer, 
        instead of the general-purpose DrawImage method.




## -see-also




<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

