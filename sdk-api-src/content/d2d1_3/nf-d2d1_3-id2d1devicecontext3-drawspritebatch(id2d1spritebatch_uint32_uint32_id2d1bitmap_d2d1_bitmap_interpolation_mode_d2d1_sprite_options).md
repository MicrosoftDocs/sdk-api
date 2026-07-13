---
UID: NF:d2d1_3.ID2D1DeviceContext3.DrawSpriteBatch(ID2D1SpriteBatch,UINT32,UINT32,ID2D1Bitmap,D2D1_BITMAP_INTERPOLATION_MODE,D2D1_SPRITE_OPTIONS)
title: ID2D1DeviceContext3::DrawSpriteBatch(ID2D1SpriteBatch,UINT32,UINT32,ID2D1Bitmap,D2D1_BITMAP_INTERPOLATION_MODE,D2D1_SPRITE_OPTIONS) (d2d1_3.h)
description: Renders part or all of the given sprite batch to the device context using the specified drawing options. (overload 1/2)
helpviewer_keywords: ["DrawSpriteBatch","DrawSpriteBatch method [Direct2D]","DrawSpriteBatch method [Direct2D]","ID2D1DeviceContext3 interface","ID2D1DeviceContext3 interface [Direct2D]","DrawSpriteBatch method","ID2D1DeviceContext3.DrawSpriteBatch","ID2D1DeviceContext3.DrawSpriteBatch(ID2D1SpriteBatch","UINT32","UINT32","ID2D1Bitmap","D2D1_BITMAP_INTERPOLATION_MODE","D2D1_SPRITE_OPTIONS)","ID2D1DeviceContext3::DrawSpriteBatch","ID2D1DeviceContext3::DrawSpriteBatch(ID2D1SpriteBatch","UINT32","UINT32","ID2D1Bitmap","D2D1_BITMAP_INTERPOLATION_MODE","D2D1_SPRITE_OPTIONS)","d2d1_3/ID2D1DeviceContext3::DrawSpriteBatch","direct2d.id2d1devicecontext3_drawspritebatch"]
old-location: direct2d\id2d1devicecontext3_drawspritebatch.htm
tech.root: Direct2D
ms.assetid: 407529D4-6FA3-4C09-876C-03A8A8D1390D
ms.date: 12/05/2018
ms.keywords: DrawSpriteBatch, DrawSpriteBatch method [Direct2D], DrawSpriteBatch method [Direct2D],ID2D1DeviceContext3 interface, ID2D1DeviceContext3 interface [Direct2D],DrawSpriteBatch method, ID2D1DeviceContext3.DrawSpriteBatch, ID2D1DeviceContext3.DrawSpriteBatch(ID2D1SpriteBatch,UINT32,UINT32,ID2D1Bitmap,D2D1_BITMAP_INTERPOLATION_MODE,D2D1_SPRITE_OPTIONS), ID2D1DeviceContext3::DrawSpriteBatch, ID2D1DeviceContext3::DrawSpriteBatch(ID2D1SpriteBatch,UINT32,UINT32,ID2D1Bitmap,D2D1_BITMAP_INTERPOLATION_MODE,D2D1_SPRITE_OPTIONS), d2d1_3/ID2D1DeviceContext3::DrawSpriteBatch, direct2d.id2d1devicecontext3_drawspritebatch
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
 - ID2D1DeviceContext3::DrawSpriteBatch
 - d2d1_3/ID2D1DeviceContext3::DrawSpriteBatch
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
 - ID2D1DeviceContext3.DrawSpriteBatch
---

# ID2D1DeviceContext3::DrawSpriteBatch(ID2D1SpriteBatch,UINT32,UINT32,ID2D1Bitmap,D2D1_BITMAP_INTERPOLATION_MODE,D2D1_SPRITE_OPTIONS)


## -description

Renders part or all of the given sprite batch to the device context using the specified drawing options.

## -parameters

### -param spriteBatch [in]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1spritebatch">ID2D1SpriteBatch</a>*</b>

The sprite batch to draw.

### -param startIndex

Type: <b>UINT32</b>

The index of the first sprite in the sprite batch to draw.

### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to draw.

### -param bitmap [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap from which the sprites are to be sourced. Each sprite's source rectangle refers to a portion of this bitmap.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use when drawing this sprite batch. This determines how Direct2D interpolates pixels within the drawn sprites if scaling is performed.

### -param spriteOptions

Type: <b><a href="/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_sprite_options">D2D1_SPRITE_OPTIONS</a></b>

The additional drawing options, if any, to be used for this sprite batch.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext3">ID2D1DeviceContext3</a>
