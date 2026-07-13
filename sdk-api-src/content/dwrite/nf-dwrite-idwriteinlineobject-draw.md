---
UID: NF:dwrite.IDWriteInlineObject.Draw
title: IDWriteInlineObject::Draw (dwrite.h)
description: The application implemented rendering callback (IDWriteTextRenderer::DrawInlineObject) can use this to draw the inline object without needing to cast or query the object type. The text layout does not call this method directly.
helpviewer_keywords: ["Draw","Draw method [Direct Write]","Draw method [Direct Write]","IDWriteInlineObject interface","IDWriteInlineObject interface [Direct Write]","Draw method","IDWriteInlineObject.Draw","IDWriteInlineObject::Draw","directwrite.IDWriteInlineObject_Draw","dwrite/IDWriteInlineObject::Draw"]
old-location: directwrite\IDWriteInlineObject_Draw.htm
tech.root: DirectWrite
ms.assetid: cbaa3341-e43a-4d3f-89c7-dda758a63e7d
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Direct Write], Draw method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],Draw method, IDWriteInlineObject.Draw, IDWriteInlineObject::Draw, directwrite.IDWriteInlineObject_Draw, dwrite/IDWriteInlineObject::Draw
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
 - IDWriteInlineObject::Draw
 - dwrite/IDWriteInlineObject::Draw
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
 - IDWriteInlineObject.Draw
---

# IDWriteInlineObject::Draw


## -description

 The application implemented rendering callback (<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject">IDWriteTextRenderer::DrawInlineObject</a>)
     can use this to draw the inline object without needing to cast or query the object
     type. The text layout does not call this method directly.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The drawing context passed to <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a>.  This parameter may be <b>NULL</b>.

### -param renderer

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a>*</b>

The same renderer passed to <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> as the object's containing parent.  This is useful if the inline object is recursive such as a nested layout.

### -param originX

Type: <b>FLOAT</b>

The x-coordinate at the upper-left corner of the inline object.

### -param originY

Type: <b>FLOAT</b>

The y-coordinate at the upper-left corner of the inline object.

### -param isSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object's baseline runs alongside the baseline axis of the line.

### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is in a right-to-left context and should be drawn flipped.

### -param clientDrawingEffect

Type: <b>IUnknown*</b>

The drawing effect set in <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect">IDWriteTextLayout::SetDrawingEffect</a>.  Usually this effect is a foreground brush that  is used in glyph drawing.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>

