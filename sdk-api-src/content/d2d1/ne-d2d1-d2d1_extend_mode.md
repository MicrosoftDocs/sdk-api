---
UID: NE:d2d1.D2D1_EXTEND_MODE
title: D2D1_EXTEND_MODE (d2d1.h)
description: Specifies how a brush paints areas outside of its normal content area.
helpviewer_keywords: ["D2D1_EXTEND_MODE","D2D1_EXTEND_MODE enumeration [Direct2D]","D2D1_EXTEND_MODE_CLAMP","D2D1_EXTEND_MODE_MIRROR","D2D1_EXTEND_MODE_WRAP","d2d1/D2D1_EXTEND_MODE","d2d1/D2D1_EXTEND_MODE_CLAMP","d2d1/D2D1_EXTEND_MODE_MIRROR","d2d1/D2D1_EXTEND_MODE_WRAP","direct2d.D2D1_EXTEND_MODE"]
old-location: direct2d\D2D1_EXTEND_MODE.htm
tech.root: Direct2D
ms.assetid: 6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4
ms.date: 12/05/2018
ms.keywords: D2D1_EXTEND_MODE, D2D1_EXTEND_MODE enumeration [Direct2D], D2D1_EXTEND_MODE_CLAMP, D2D1_EXTEND_MODE_MIRROR, D2D1_EXTEND_MODE_WRAP, d2d1/D2D1_EXTEND_MODE, d2d1/D2D1_EXTEND_MODE_CLAMP, d2d1/D2D1_EXTEND_MODE_MIRROR, d2d1/D2D1_EXTEND_MODE_WRAP, direct2d.D2D1_EXTEND_MODE
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_EXTEND_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_EXTEND_MODE
 - d2d1/D2D1_EXTEND_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_EXTEND_MODE
---

# D2D1_EXTEND_MODE enumeration


## -description

Specifies how a brush paints areas outside of its normal content area.

## -enum-fields

### -field D2D1_EXTEND_MODE_CLAMP:0

Repeat the edge pixels of the brush's content for all regions outside the normal content area.

### -field D2D1_EXTEND_MODE_WRAP:1

Repeat the brush's content.

### -field D2D1_EXTEND_MODE_MIRROR:2

 The same as D2D1_EXTEND_MODE_WRAP, except that alternate tiles of the brush's content are flipped. (The brush's normal content is drawn untransformed.)

### -field D2D1_EXTEND_MODE_FORCE_DWORD:0xffffffff

## -remarks

For an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>, the brush's content is the brush's bitmap. For an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>, the brush's content area is the gradient axis. For an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>, the brush's content is the area within the gradient ellipse.

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex">ID2D1BitmapBrush::SetExtendModeX</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey">ID2D1BitmapBrush::SetExtendModeY</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>

