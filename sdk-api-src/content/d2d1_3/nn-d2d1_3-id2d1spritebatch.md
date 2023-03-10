---
UID: NN:d2d1_3.ID2D1SpriteBatch
title: ID2D1SpriteBatch (d2d1_3.h)
description: Represents a single group of sprites with their associated drawing properties.
helpviewer_keywords: ["ID2D1SpriteBatch","ID2D1SpriteBatch interface [Direct2D]","ID2D1SpriteBatch interface [Direct2D]","described","d2d1_3/ID2D1SpriteBatch","direct2d.id2d1spritebatch"]
old-location: direct2d\id2d1spritebatch.htm
tech.root: Direct2D
ms.assetid: D33958D5-D31C-47DC-B172-CADB1F1B81AE
ms.date: 12/05/2018
ms.keywords: ID2D1SpriteBatch, ID2D1SpriteBatch interface [Direct2D], ID2D1SpriteBatch interface [Direct2D],described, d2d1_3/ID2D1SpriteBatch, direct2d.id2d1spritebatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SpriteBatch
 - d2d1_3/ID2D1SpriteBatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SpriteBatch
---

# ID2D1SpriteBatch interface


## -description

Represents a single group of sprites with their associated drawing properties.

## -inheritance

The <b>ID2D1SpriteBatch</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1SpriteBatch</b> also has these types of members:

## -remarks

Create a new sprite batch using <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch">ID2D1DeviceContext3::CreateSpriteBatch</a>. 
          Use [ID2D1DeviceContext3::DrawSpriteBatch](./nf-d2d1_3-id2d1devicecontext3-createspritebatch.md) to draw them.
        

Sprites are a way for apps to draw a large number of images very efficiently. 
        They are commonly used to render characters and backgrounds in 2D games, or to render particle systems such as smoke and flames. 
        If your app has performance demands and needs to draw hundreds or thousands of images every frame, then consider taking advantage of sprite batches and the fine-grained control they offer, 
        instead of the general-purpose DrawImage method.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>
