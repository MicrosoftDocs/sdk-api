---
UID: NF:d2d1_3.ID2D1SpriteBatch.SetSprites
title: ID2D1SpriteBatch::SetSprites (d2d1_3.h)
description: Updates the properties of the specified sprites in this sprite batch.
helpviewer_keywords: ["ID2D1SpriteBatch interface [Direct2D]","SetSprites method","ID2D1SpriteBatch.SetSprites","ID2D1SpriteBatch::SetSprites","SetSprites","SetSprites method [Direct2D]","SetSprites method [Direct2D]","ID2D1SpriteBatch interface","d2d1_3/ID2D1SpriteBatch::SetSprites","direct2d.id2d1spritebatch_setsprites"]
old-location: direct2d\id2d1spritebatch_setsprites.htm
tech.root: Direct2D
ms.assetid: 6BC5740F-520D-47EA-A90A-973E158F2AC2
ms.date: 12/05/2018
ms.keywords: ID2D1SpriteBatch interface [Direct2D],SetSprites method, ID2D1SpriteBatch.SetSprites, ID2D1SpriteBatch::SetSprites, SetSprites, SetSprites method [Direct2D], SetSprites method [Direct2D],ID2D1SpriteBatch interface, d2d1_3/ID2D1SpriteBatch::SetSprites, direct2d.id2d1spritebatch_setsprites
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
 - ID2D1SpriteBatch::SetSprites
 - d2d1_3/ID2D1SpriteBatch::SetSprites
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
 - ID2D1SpriteBatch.SetSprites
---

# ID2D1SpriteBatch::SetSprites


## -description

Updates the properties of the specified sprites in this sprite batch.Providing a null value for any property will leave that property unmodified for that sprite.

## -parameters

### -param startIndex

Type: <b>UINT32</b>

The index of the first sprite in this sprite batch to update.

### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to update with new properties. This determines how many strides into each given array Direct2D will read.

### -param destinationRectangles [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

A pointer to an array containing the destination rectangles specifying where to draw the sprites on the destination device context.

### -param sourceRectangles [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a>*</b>

A pointer to an array containing the source rectangles specifying the regions of the source bitmap to draw as sprites.

          

Direct2D will use the entire source bitmap for sprites that are assigned a null value or the InfiniteRectU. 
          If this parameter is omitted entirely or set to a null value, then Direct2D will use the entire source bitmap for all the updated sprites.

### -param colors [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a>*</b>

A pointer to an array containing the colors to apply to each sprite. The output color is the result of component-wise multiplication of the source bitmap color and the provided color. 
          The output color is not clamped.

          

Direct2D will not change the color of sprites that are assigned a null value. If this parameter is omitted entirely or set to a null value, 
          then Direct2D will not change the color of any of the updated sprites.

### -param transforms [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

A pointer to an array containing the transforms to apply to each sprite’s destination rectangle.

          

Direct2D will not transform the destination rectangle of any sprites that are assigned a null value. 
          If this parameter is omitted entirely or set to a null value, then Direct2D will not transform the destination rectangle of any of the updated sprites.

### -param destinationRectanglesStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each rectangle in the destinationRectangles array. 
          If you provide a stride of 0, then the same destination rectangle will be used for each updated sprite.

### -param sourceRectanglesStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each rectangle in the sourceRectangles array (if that array is given). 
          If you provide a stride of 0, then the same source rectangle will be used for each updated sprite.

### -param colorsStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each color in the colors array (if that array is given). 
          If you provide a stride of 0, then the same color will be used for each updated sprite.

### -param transformsStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each transform in the transforms array (if that array is given). 
          If you provide a stride of 0, then the same transform will be used for each updated sprite.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on success. Returns E_INVALIDARG if an invalid value was passed to the method. In this case, no sprites are modified by this call to SetSprites.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1spritebatch">ID2D1SpriteBatch</a>