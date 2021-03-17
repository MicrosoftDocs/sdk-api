---
UID: NF:d2d1_1.ID2D1DeviceContext.GetTarget
title: ID2D1DeviceContext::GetTarget (d2d1_1.h)
description: Gets the target currently associated with the device context.
helpviewer_keywords: ["GetTarget","GetTarget method [Direct2D]","GetTarget method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetTarget method","ID2D1DeviceContext.GetTarget","ID2D1DeviceContext::GetTarget","d2d1_1/ID2D1DeviceContext::GetTarget","direct2d.id2d1devicecontext_gettarget"]
old-location: direct2d\id2d1devicecontext_gettarget.htm
tech.root: Direct2D
ms.assetid: a70307db-863a-4c59-a327-fb71a5d58f84
ms.date: 12/05/2018
ms.keywords: GetTarget, GetTarget method [Direct2D], GetTarget method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetTarget method, ID2D1DeviceContext.GetTarget, ID2D1DeviceContext::GetTarget, d2d1_1/ID2D1DeviceContext::GetTarget, direct2d.id2d1devicecontext_gettarget
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
 - ID2D1DeviceContext::GetTarget
 - d2d1_1/ID2D1DeviceContext::GetTarget
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
 - ID2D1DeviceContext.GetTarget
---

# ID2D1DeviceContext::GetTarget


## -description

Gets the target currently associated with the device context.

## -parameters

### -param image [out, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the target currently associated with the device context.

## -remarks

If a target is not associated with the device context, <i>target</i> will contain <b>NULL</b> when the methods returns.

If the currently selected target is a bitmap rather than a command list, the application can gain access to the initial bitmaps created by using one of the following methods:

<ul>
<li>
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties_constd2d1_hwnd_render_target_properties_id2d1hwndrendertarget)">CreateHwndRenderTarget</a>
</li>
<li>
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties_id2d1rendertarget)">CreateDxgiSurfaceRenderTarget</a>
</li>
<li>
<a href="/windows/desktop/Direct2D/id2d1factory-createwicbitmaprendertarget">CreateWicBitmapRenderTarget</a>
</li>
<li>
<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget">CreateDCRenderTarget</a>
</li>
<li>
<a href="/windows/win32/direct2d/id2d1rendertarget-createcompatiblerendertarget">CreateCompatibleRenderTarget</a>
</li>
</ul>
It is not possible for an application to destroy these bitmaps.  All of these bitmaps are bindable as bitmap targets.  However not all of these bitmaps can be used as bitmap sources for  <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> methods.


<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties_id2d1rendertarget)">CreateDxgiSurfaceRenderTarget</a> will create a bitmap that is usable as a bitmap source if the DXGI surface is bindable as a shader resource view.


<a href="/windows/win32/direct2d/id2d1rendertarget-createcompatiblerendertarget">CreateCompatibleRenderTarget</a> will always create bitmaps that are usable as a bitmap source.


<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">ID2D1RenderTarget::BeginDraw</a> will copy from the HDC to the original bitmap associated with it.  <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> will copy from the original bitmap to the HDC.  


<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> objects will be locked in the following circumstances:

<ul>
<li>BeginDraw has been called and the currently selected target bitmap is a WIC bitmap.</li>
<li>A WIC bitmap is set as the target of a device context after BeginDraw has been called and before EndDraw has been called.</li>
<li>Any of the ID2D1Bitmap::Copy* methods are called with a WIC bitmap as either the source or destination.</li>
</ul>
IWICBitmap objects will be unlocked in the following circumstances:

<ul>
<li>EndDraw is called and the currently selected target bitmap is a WIC bitmap.</li>
<li>A WIC bitmap is removed as the target of a device context between the calls to BeginDraw and EndDraw.</li>
<li>Any of the ID2D1Bitmap::Copy* methods are called with a WIC bitmap as either the source or destination.</li>
</ul>
Direct2D will only lock bitmaps that are not currently locked.

Calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget">ID2D1GdiInteropRenderTarget</a> will always succeed.  <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">ID2D1GdiInteropRenderTarget::GetDC</a> will return a device context corresponding to the currently bound target bitmap.  GetDC will fail if the target bitmap was not created with the GDI_COMPATIBLE flag set.


<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)">ID2D1HwndRenderTarget::Resize</a> will return <b>DXGI_ERROR_INVALID_CALL</b> if there are any outstanding references to the original target bitmap associated with the render target.

Although the target can be a command list, it cannot be any other type of image. It cannot be the output image of an effect.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget">ID2D1DeviceContext::SetTarget</a>