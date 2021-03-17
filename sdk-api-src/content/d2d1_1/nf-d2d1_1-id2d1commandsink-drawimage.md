---
UID: NF:d2d1_1.ID2D1CommandSink.DrawImage
title: ID2D1CommandSink::DrawImage (d2d1_1.h)
description: Draws the provided image to the command sink.
helpviewer_keywords: ["DrawImage","DrawImage method [Direct2D]","DrawImage method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawImage method","ID2D1CommandSink.DrawImage","ID2D1CommandSink::DrawImage","d2d1_1/ID2D1CommandSink::DrawImage","direct2d.id2d1commandsink_drawimage"]
old-location: direct2d\id2d1commandsink_drawimage.htm
tech.root: Direct2D
ms.assetid: 1235dd6d-8495-4a92-96b7-4d741d9e296f
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [Direct2D], DrawImage method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawImage method, ID2D1CommandSink.DrawImage, ID2D1CommandSink::DrawImage, d2d1_1/ID2D1CommandSink::DrawImage, direct2d.id2d1commandsink_drawimage
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
 - ID2D1CommandSink::DrawImage
 - d2d1_1/ID2D1CommandSink::DrawImage
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
 - ID2D1CommandSink.DrawImage
---

# ID2D1CommandSink::DrawImage


## -description

Draws the provided image to the command sink.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The image to be drawn to the command sink.

### -param targetOffset [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

This defines the offset in the destination space that the image will be rendered to. The entire logical extent of the image will be rendered to the corresponding destination. If not specified, the destination origin will be (0, 0). The top-left corner of the image will be mapped to the target offset. This will not necessarily be the origin.

### -param imageRectangle [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The corresponding rectangle in the image space will be mapped to the provided origins when processing the image.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use to  scale the image if necessary.

### -param compositeMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_composite_mode">D2D1_COMPOSITE_MODE</a></b>

If specified, the composite mode that will be applied to the limits of the currently selected clip.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Because the image can itself be a command list or contain an effect graph that in turn contains a command list, this method can result in recursive processing.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>