---
UID: NF:d2d1.ID2D1RenderTarget.FillEllipse(constD2D1_ELLIPSE&,ID2D1Brush)
title: ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush) (d2d1.h)
description: Paints the interior of the specified ellipse. (overload 1/2)
helpviewer_keywords: ["FillEllipse","FillEllipse method [Direct2D]","FillEllipse method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillEllipse method","ID2D1RenderTarget.FillEllipse","ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &","ID2D1Brush)","ID2D1RenderTarget::FillEllipse","ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &","ID2D1Brush)","d2d1/ID2D1RenderTarget::FillEllipse","direct2d.ID2D1RenderTarget_FillEllipse_ref_D2D1_ELLIPSE_ptr_ID2D1Brush"]
old-location: direct2d\ID2D1RenderTarget_FillEllipse_ref_D2D1_ELLIPSE_ptr_ID2D1Brush.htm
tech.root: Direct2D
ms.assetid: 007c5733-91d4-42c8-bd76-ae10225d3d5e
ms.date: 12/05/2018
ms.keywords: FillEllipse, FillEllipse method [Direct2D], FillEllipse method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillEllipse method, ID2D1RenderTarget.FillEllipse, ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), ID2D1RenderTarget::FillEllipse, ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), d2d1/ID2D1RenderTarget::FillEllipse, direct2d.ID2D1RenderTarget_FillEllipse_ref_D2D1_ELLIPSE_ptr_ID2D1Brush
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
 - ID2D1RenderTarget::FillEllipse
 - d2d1/ID2D1RenderTarget::FillEllipse
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
 - ID2D1RenderTarget.FillEllipse
---

## -description

Paints the interior of the specified ellipse.

## -parameters

### -param ellipse

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a> &</b>

The position and radius, in device-independent pixels, of the ellipse to paint.

### -param brush

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the interior of the ellipse.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush)">FillEllipse</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 

## Examples

For an example, see <a href="/windows/win32/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>.

## -see-also

<a href="/windows/win32/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

