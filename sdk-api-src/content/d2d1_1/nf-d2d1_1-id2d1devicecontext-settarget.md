---
UID: NF:d2d1_1.ID2D1DeviceContext.SetTarget
title: ID2D1DeviceContext::SetTarget (d2d1_1.h)
description: The bitmap or command list to which the Direct2D device context will now render.
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","SetTarget method","ID2D1DeviceContext.SetTarget","ID2D1DeviceContext::SetTarget","SetTarget","SetTarget method [Direct2D]","SetTarget method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::SetTarget","direct2d.id2d1devicecontext_settarget"]
old-location: direct2d\id2d1devicecontext_settarget.htm
tech.root: Direct2D
ms.assetid: 66914048-7bef-4551-bb14-5ab67c727dc5
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],SetTarget method, ID2D1DeviceContext.SetTarget, ID2D1DeviceContext::SetTarget, SetTarget, SetTarget method [Direct2D], SetTarget method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::SetTarget, direct2d.id2d1devicecontext_settarget
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
 - ID2D1DeviceContext::SetTarget
 - d2d1_1/ID2D1DeviceContext::SetTarget
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
 - ID2D1DeviceContext.SetTarget
---

# ID2D1DeviceContext::SetTarget


## -description

The bitmap or command list to which the <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device context will now render.

## -parameters

### -param image [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The surface or command list to which the Direct2D device context will render.

## -remarks

The target can be changed at any time, including while the context is drawing.

The target can be either a bitmap created with the <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS_TARGET</a> flag, or it can be a command list. Other kinds of images cannot be set as a target. For example, you cannot set the output of an effect as target. If the target is not valid the context will enter the <b>D2DERR_INVALID_TARGET </b> error state.

You cannot  use <b>SetTarget</b> to render to a bitmap/command list from multiple device contexts simultaneously. An image is considered “being rendered to” if it has ever been set on a device context within a <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a>/<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> timespan. If an attempt is made to render to an image through multiple device contexts, all subsequent device contexts after the first will enter an error state.



Callers wishing to attach an image to a second device context should first call <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> on the first device context.


Here is an example of the correct calling order.


```cpp
pDC1->BeginDraw();
pDC1->SetTarget(pImage);
// …
pDC1->EndDraw();

pDC2->BeginDraw();
pDC2->SetTarget(pImage);
// …
pDC2->EndDraw();

```


Here is an example of the incorrect calling order.


```cpp
pDC1->BeginDraw();
pDC2->BeginDraw();

pDC1->SetTarget(pImage);

// ...

pDC1->SetTarget(NULL);

pDC2->SetTarget(pImage); // This call is invalid, even though pImage is no longer set on pDC1.

// ...

pDC1->EndDraw(); // This EndDraw SUCCEEDs.
pDC2->EndDraw(); // This EndDraw FAILs


```


<div class="alert"><b>Note</b>  Changing the target does not change the bitmap that an HWND render target presents from, nor does it change the bitmap that a DC render target blts to/from.</div>
<div> </div>
This API makes it easy for an application to use a bitmap as a source (like in <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawbitmap">DrawBitmap</a>) and as a destination at the same time.  Attempting to use a bitmap as a source on the same device context to which it is bound as a target will put the device context into the D2DERR_BITMAP_BOUND_AS_TARGET error state.

It is acceptable to have a bitmap bound as a target bitmap on multiple render targets at once.  Applications that do this must properly synchronize rendering with <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> or <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a>.

You can change the target at any time, including while the context is drawing.

You can set the target to NULL, in which case drawing calls will put the device context into an error state with D2DERR_WRONG_STATE.  Calling <b>SetTarget</b> with a NULL target does not restore the original target bitmap to the device context.

If the device context has an outstanding HDC, the context will enter the <b>D2DERR_WRONG_STATE</b> error state.  The target will not be changed.

If the bitmap and the device context are not in the same resource domain, the context will enter <b>\\</b> error state.  The target will not be changed.


<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize">ID2D1RenderTarget::GetPixelSize</a> returns the size of the current target bitmap (or 0, 0) if there is no bitmap bound).
<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize">ID2D1RenderTarget::GetSize</a> returns the pixel size of the current bitmap scaled by the DPI of the render target.
<b>SetTarget</b> does not affect the DPI of the render target.



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat">ID2D1RenderTarget::GetPixelFormat</a> returns the pixel format of the current target bitmap (or <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a>, <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a> if there is none).


<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget">ID2D1Bitmap::CopyFromRenderTarget</a> copies from the currently bound target bitmap.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-gettarget">ID2D1DeviceContext::GetTarget</a>