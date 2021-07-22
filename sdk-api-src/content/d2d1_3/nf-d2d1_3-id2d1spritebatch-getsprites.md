---
UID: NF:d2d1_3.ID2D1SpriteBatch.GetSprites
title: ID2D1SpriteBatch::GetSprites (d2d1_3.h)
description: Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.
helpviewer_keywords: ["GetSprites","GetSprites method [Direct2D]","GetSprites method [Direct2D]","ID2D1SpriteBatch interface","ID2D1SpriteBatch interface [Direct2D]","GetSprites method","ID2D1SpriteBatch.GetSprites","ID2D1SpriteBatch::GetSprites","d2d1_3/ID2D1SpriteBatch::GetSprites","direct2d.id2d1spritebatch_getsprites"]
old-location: direct2d\id2d1spritebatch_getsprites.htm
tech.root: Direct2D
ms.assetid: 39B6D8ED-25B2-4542-8994-FD607E60E19A
ms.date: 12/05/2018
ms.keywords: GetSprites, GetSprites method [Direct2D], GetSprites method [Direct2D],ID2D1SpriteBatch interface, ID2D1SpriteBatch interface [Direct2D],GetSprites method, ID2D1SpriteBatch.GetSprites, ID2D1SpriteBatch::GetSprites, d2d1_3/ID2D1SpriteBatch::GetSprites, direct2d.id2d1spritebatch_getsprites
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
 - ID2D1SpriteBatch::GetSprites
 - d2d1_3/ID2D1SpriteBatch::GetSprites
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
 - ID2D1SpriteBatch.GetSprites
---

# ID2D1SpriteBatch::GetSprites


## -description

Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.

## -parameters

### -param startIndex

Type: <b>UINT32</b>

The index of the first sprite in this sprite batch to retrieve.

### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to retrieve.

### -param destinationRectangles [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

When this method returns, contains a pointer to an array containing the destination rectangles for the retrieved sprites.

### -param sourceRectangles [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a>*</b>

When this method returns, contains a pointer to an array containing the source rectangles for the retrieved sprites.

          

The InfiniteRectU is returned for any sprites that were not assigned a source rectangle.

### -param colors [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a>*</b>

When this method returns, contains a pointer to an array containing the colors to be applied to the retrieved sprites.

          

The color {1.0f, 1.0f, 1.0f, 1.0f} is returned for any sprites that were not assigned a color.

### -param transforms [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains a pointer to an array containing the transforms to be applied to the retrieved sprites.

            

The identity matrix is returned for any sprites that were not assigned a transform.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1spritebatch">ID2D1SpriteBatch</a>