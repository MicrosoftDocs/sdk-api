---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawImage(ID2D1Image,D2D1_POINT_2F,constD2D1_RECT_F&,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE)
title: ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,const D2D1_RECT_F &,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE) (d2d1_1.h)
description: Draws an image to the device context. (overload 3/8)
helpviewer_keywords: ["DrawImage","DrawImage method [Direct2D]","DrawImage method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","DrawImage method","ID2D1DeviceContext.DrawImage","ID2D1DeviceContext.DrawImage(ID2D1Image","D2D1_POINT_2F","const D2D1_RECT_F &","D2D1_INTERPOLATION_MODE","D2D1_COMPOSITE_MODE)","ID2D1DeviceContext::DrawImage","ID2D1DeviceContext::DrawImage(ID2D1Image","D2D1_POINT_2F","const D2D1_RECT_F &","D2D1_INTERPOLATION_MODE","D2D1_COMPOSITE_MODE)","d2d1_1/ID2D1DeviceContext::DrawImage","direct2d.id2d1devicecontext_drawimage7"]
old-location: direct2d\id2d1devicecontext_drawimage7.htm
tech.root: Direct2D
ms.assetid: 52EB16C9-7C90-45E7-8ED3-D2489765ADA6
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [Direct2D], DrawImage method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawImage method, ID2D1DeviceContext.DrawImage, ID2D1DeviceContext.DrawImage(ID2D1Image,D2D1_POINT_2F,const D2D1_RECT_F &,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE), ID2D1DeviceContext::DrawImage, ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,const D2D1_RECT_F &,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE), d2d1_1/ID2D1DeviceContext::DrawImage, direct2d.id2d1devicecontext_drawimage7
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::DrawImage
 - d2d1_1/ID2D1DeviceContext::DrawImage
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
 - ID2D1DeviceContext.DrawImage
---

# ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,const D2D1_RECT_F &,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE)


## -description

Draws an image to the device context.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The image to be drawn to the device context.

### -param targetOffset [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

The  offset in the destination space that the image will be rendered to. The entire logical extent of the image will be rendered to the corresponding destination. If not specified, the destination origin will be (0, 0). The top-left corner of the image will be mapped to the target offset. This will not necessarily be the origin. This default value is <i>NULL</i>.

### -param imageRectangle [in, ref, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The corresponding rectangle in the image space will be mapped to the given origins when processing the image. This default value is <i>NULL</i>.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode that will be used to scale the image if necessary.

### -param compositeMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_composite_mode">D2D1_COMPOSITE_MODE</a></b>

The composite mode that will be applied to the limits of the currently selected clip. The default value is <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>

## -remarks

If <i>interpolationMode</i> is <b>D2D1_INTERPOLATION_MODE_HIGH_QUALITY</b>, different scalers will be used depending on the scale factor implied by the world transform.

Any invalid rectangles accumulated on any effect that is drawn by this call will be discarded regardless of which portion of the image rectangle is drawn.

If <i>compositeMode</i> is <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>, <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">DrawImage</a> will use the currently selected primitive blend specified by <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setprimitiveblend">ID2D1DeviceContext::SetPrimitiveBlend</a>. If <i>compositeMode</i> is not <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>, the image will be extended to transparent up to the current axis-aligned clip.

If there is an image rectangle and a world transform, this is equivalent to inserting a clip effect to represent the image rectangle and a 2D affine transform to take into account the world transform.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>
