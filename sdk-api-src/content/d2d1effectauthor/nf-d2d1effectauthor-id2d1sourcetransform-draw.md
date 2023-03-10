---
UID: NF:d2d1effectauthor.ID2D1SourceTransform.Draw
title: ID2D1SourceTransform::Draw (d2d1effectauthor.h)
description: Draws the transform to the graphics processing unit (GPU)–based Direct2D pipeline.
helpviewer_keywords: ["Draw","Draw method [Direct2D]","Draw method [Direct2D]","ID2D1SourceTransform interface","ID2D1SourceTransform interface [Direct2D]","Draw method","ID2D1SourceTransform.Draw","ID2D1SourceTransform::Draw","d2d1effectauthor/ID2D1SourceTransform::Draw","direct2d.id2d1sourcetransform_draw"]
old-location: direct2d\id2d1sourcetransform_draw.htm
tech.root: Direct2D
ms.assetid: 38EBBFB2-7A49-4386-80B3-86B44BF2FC39
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Direct2D], Draw method [Direct2D],ID2D1SourceTransform interface, ID2D1SourceTransform interface [Direct2D],Draw method, ID2D1SourceTransform.Draw, ID2D1SourceTransform::Draw, d2d1effectauthor/ID2D1SourceTransform::Draw, direct2d.id2d1sourcetransform_draw
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SourceTransform::Draw
 - d2d1effectauthor/ID2D1SourceTransform::Draw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1SourceTransform.Draw
---

# ID2D1SourceTransform::Draw


## -description

Draws the transform to the graphics processing unit (GPU)–based Direct2D pipeline.

## -parameters

### -param target [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>*</b>

The target to which the transform should be written.

### -param drawRect [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

The area within the source from which the image should be drawn.

### -param targetOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2u">D2D1_POINT_2U</a></b>

The origin within the target bitmap to which the source data should be drawn.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The implementation of the rasterizer guarantees that adding the <i>renderRect</i> to the <i>targetOrigin</i> does not exceed the bounds of the bitmap.

When implementing this method you must update the bitmap in this way: 

<ol>
<li>Call the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map">ID2D1Bitmap::Map</a> method with the  D2D1_MAP_OPTIONS_DISCARD and D2D1_MAP_OPTIONS_WRITE
flags.</li>
<li>Update the buffer this method returns.</li>
<li>Call the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-unmap">ID2D1Bitmap::Unmap</a> method.</li>
</ol>
If you  set the buffer precision manually on the associated <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1renderinfo">ID2D1RenderInfo</a> object, it must handle different pixel formats in this method by calling <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmap-getpixelformat">ID2D1Bitmap::GetPixelFormat</a>.  If you set the buffer precision manually, then you can rely on that format always being the one you provided.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1sourcetransform">ID2D1SourceTransform</a>