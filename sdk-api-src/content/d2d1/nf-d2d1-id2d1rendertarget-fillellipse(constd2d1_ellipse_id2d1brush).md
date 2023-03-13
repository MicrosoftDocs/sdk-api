---
UID: NF:d2d1.ID2D1RenderTarget.FillEllipse(constD2D1_ELLIPSE,ID2D1Brush)
title: ID2D1RenderTarget::FillEllipse (d2d1.h)
description: Paints the interior of the specified ellipse. (overload 2/2)
helpviewer_keywords: ["FillEllipse","FillEllipse methods [Direct2D]","ID2D1RenderTarget.FillEllipse","ID2D1RenderTarget::FillEllipse","d2d1/FillEllipse","direct2d.id2d1rendertarget_fillellipse"]
old-location: direct2d\id2d1rendertarget_fillellipse.htm
tech.root: Direct2D
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
ms.date: 12/05/2018
ms.keywords: FillEllipse, FillEllipse methods [Direct2D], ID2D1RenderTarget.FillEllipse, ID2D1RenderTarget::FillEllipse, d2d1/FillEllipse, direct2d.id2d1rendertarget_fillellipse
req.header: d2d1.h
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
 - ID2D1RenderTarget::FillEllipse
 - d2d1/ID2D1RenderTarget::FillEllipse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::FillEllipse
---

## -description

Paints the interior of the specified ellipse.

## -parameters

### -param ellipse

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a>*</b>

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

