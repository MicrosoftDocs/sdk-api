---
UID: NF:d2d1.ID2D1RenderTarget.FillGeometry
title: ID2D1RenderTarget::FillGeometry (d2d1.h)
description: Paints the interior of the specified geometry.
helpviewer_keywords: ["FillGeometry","FillGeometry method [Direct2D]","FillGeometry method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillGeometry method","ID2D1RenderTarget.FillGeometry","ID2D1RenderTarget::FillGeometry","d2d1/ID2D1RenderTarget::FillGeometry","direct2d.ID2D1RenderTarget_FillGeometry"]
old-location: direct2d\ID2D1RenderTarget_FillGeometry.htm
tech.root: Direct2D
ms.assetid: 097f21ac-a062-4ce1-bdc7-87317dbdf5be
ms.date: 12/05/2018
ms.keywords: FillGeometry, FillGeometry method [Direct2D], FillGeometry method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillGeometry method, ID2D1RenderTarget.FillGeometry, ID2D1RenderTarget::FillGeometry, d2d1/ID2D1RenderTarget::FillGeometry, direct2d.ID2D1RenderTarget_FillGeometry
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
 - ID2D1RenderTarget::FillGeometry
 - d2d1/ID2D1RenderTarget::FillGeometry
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
 - ID2D1RenderTarget.FillGeometry
---

# ID2D1RenderTarget::FillGeometry


## -description

Paints the interior of the specified geometry.

## -parameters

### -param geometry [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry to paint.

### -param brush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the geometry's interior.

### -param opacityBrush [in, optional]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The opacity mask to apply to the geometry, or <b>NULL</b> for no opacity mask. If an opacity mask (the <i>opacityBrush</i> parameter) is specified, <i>brush</i> must be an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> that has   its x- and y-extend modes set to <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a>. For more information, see the Remarks section.

## -remarks

If the <i>opacityBrush</i> parameter is not <b>NULL</b>, the alpha value of each pixel of the mapped <i>opacityBrush</i> is used to determine the resulting opacity of each corresponding pixel of the geometry. Only the alpha value of each color in the brush is used for this processing; all other color information is ignored. 

The alpha value specified by the brush is multiplied by the alpha value of the geometry after the geometry has been painted by <i>brush</i>.  


When this method fails, it does not return an error code. To determine whether a drawing operation (such as <b>FillGeometry</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> method. 


## Examples

For an example, see <a href="/windows/win32/Direct2D/how-to-draw-and-fill-a-complex-shape">How to Draw and Fill a Complex Shape</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a>



<a href="/windows/win32/Direct2D/geometries">Geometries</a>



<a href="/windows/win32/Direct2D/direct2d-geometries-overview">Geometries Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

