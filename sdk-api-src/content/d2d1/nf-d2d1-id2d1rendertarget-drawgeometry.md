---
UID: NF:d2d1.ID2D1RenderTarget.DrawGeometry
title: ID2D1RenderTarget::DrawGeometry (d2d1.h)
description: Draws the outline of the specified geometry using the specified stroke style.
helpviewer_keywords: ["DrawGeometry","DrawGeometry method [Direct2D]","DrawGeometry method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawGeometry method","ID2D1RenderTarget.DrawGeometry","ID2D1RenderTarget::DrawGeometry","d2d1/ID2D1RenderTarget::DrawGeometry","direct2d.ID2D1RenderTarget_DrawGeometry"]
old-location: direct2d\ID2D1RenderTarget_DrawGeometry.htm
tech.root: Direct2D
ms.assetid: 319b2680-34f8-4e00-985e-47ff87115794
ms.date: 12/05/2018
ms.keywords: DrawGeometry, DrawGeometry method [Direct2D], DrawGeometry method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawGeometry method, ID2D1RenderTarget.DrawGeometry, ID2D1RenderTarget::DrawGeometry, d2d1/ID2D1RenderTarget::DrawGeometry, direct2d.ID2D1RenderTarget_DrawGeometry
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::DrawGeometry
 - d2d1/ID2D1RenderTarget::DrawGeometry
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
 - ID2D1RenderTarget.DrawGeometry
---

# ID2D1RenderTarget::DrawGeometry


## -description

Draws the outline of the specified geometry using the specified stroke style.

## -parameters

### -param geometry [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry to draw.

### -param brush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the geometry's stroke.

### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply to the geometry's outline, or <b>NULL</b> to paint a solid stroke.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawGeometry</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


## Examples

For an example, see <a href="/windows/win32/Direct2D/how-to-draw-and-fill-a-complex-shape">How to Draw and Fill a Complex Shape</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/geometries">Geometries</a>



<a href="/windows/win32/Direct2D/direct2d-geometries-overview">Geometries Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

