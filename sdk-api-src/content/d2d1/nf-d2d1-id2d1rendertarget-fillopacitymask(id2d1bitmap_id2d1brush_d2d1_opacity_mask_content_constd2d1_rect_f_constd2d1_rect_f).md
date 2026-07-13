---
UID: NF:d2d1.ID2D1RenderTarget.FillOpacityMask(ID2D1Bitmap,ID2D1Brush,D2D1_OPACITY_MASK_CONTENT,constD2D1_RECT_F,constD2D1_RECT_F)
title: ID2D1RenderTarget::FillOpacityMask (d2d1.h)
description: Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target. (overload 2/2)
helpviewer_keywords: ["FillOpacityMask","FillOpacityMask method [Direct2D]","FillOpacityMask method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillOpacityMask method","ID2D1RenderTarget.FillOpacityMask","ID2D1RenderTarget::FillOpacityMask","ID2D1RenderTarget::FillOpacityMask(ID2D1Bitmap","ID2D1Brush","D2D1_OPACITY_MASK_CONTENT","const D2D1_RECT_F","const D2D1_RECT_F)","d2d1/ID2D1RenderTarget::FillOpacityMask","direct2d.ID2D1RenderTarget_FillOpacityMask_ptr_ID2D1Bitmap_ptr_ID2D1Brush_ptr_D2D_RECT_F_ptr_D2D_RECT_F_ptr_D2D1_GAMMA"]
old-location: direct2d\ID2D1RenderTarget_FillOpacityMask_ptr_ID2D1Bitmap_ptr_ID2D1Brush_ptr_D2D_RECT_F_ptr_D2D_RECT_F_ptr_D2D1_GAMMA.htm
tech.root: Direct2D
ms.assetid: 9d482d3e-f957-4dd4-ba40-c8ef9c522f72
ms.date: 12/05/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillOpacityMask method, ID2D1RenderTarget.FillOpacityMask, ID2D1RenderTarget::FillOpacityMask, ID2D1RenderTarget::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,D2D1_OPACITY_MASK_CONTENT,const D2D1_RECT_F,const D2D1_RECT_F), d2d1/ID2D1RenderTarget::FillOpacityMask, direct2d.ID2D1RenderTarget_FillOpacityMask_ptr_ID2D1Bitmap_ptr_ID2D1Brush_ptr_D2D_RECT_F_ptr_D2D_RECT_F_ptr_D2D1_GAMMA
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
 - ID2D1RenderTarget::FillOpacityMask
 - d2d1/ID2D1RenderTarget::FillOpacityMask
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
 - ID2D1RenderTarget.FillOpacityMask
---

# ID2D1RenderTarget::FillOpacityMask


## -description

Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.

## -parameters

### -param opacityMask [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The opacity mask to apply to the brush. The alpha value of each pixel in the  region specified by <i>sourceRectangle</i> is multiplied with the alpha value of the brush after the brush has been mapped to the area defined by <i>destinationRectangle</i>.

### -param brush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the region of the render target specified by <i>destinationRectangle</i>.

### -param content

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_opacity_mask_content">D2D1_OPACITY_MASK_CONTENT</a></b>

The type of content the opacity mask contains. The value is used to determine the color space in which the opacity mask is blended. 

<div class="alert"><b>Note</b>  Starting with Windows 8, the <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_opacity_mask_content">D2D1_OPACITY_MASK_CONTENT</a> is not required. See the <a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f__constd2d1_rect_f)">ID2D1DeviceContext::FillOpacityMask</a> method, which has no <b>D2D1_OPACITY_MASK_CONTENT</b> parameter.</div>
<div> </div>

### -param destinationRectangle [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The region of the render target to paint, in device-independent pixels, or <b>NULL</b>. If <b>NULL</b> is specified, the brush paints a rectangle the same size as <i>sourceRectangle</i>, but positioned on the origin. If <i>sourceRectangle</i> isn't specified, the brush paints a rectangle the same size as the <i>opacityMask</i> bitmap and positioned on the origin.

### -param sourceRectangle [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The region of the bitmap to use as the opacity mask, in device-independent pixels, or <b>NULL</b>. If <b>NULL</b> is specified, the entire bitmap is used.

## -remarks

For this method to work properly, the render target must be using the <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE_ALIASED</a> antialiasing mode. You can set the antialiasing mode by calling the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode">ID2D1RenderTarget::SetAntialiasMode</a> method.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/Direct2D/id2d1rendertarget-fillopacitymask">FillOpacityMask</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

