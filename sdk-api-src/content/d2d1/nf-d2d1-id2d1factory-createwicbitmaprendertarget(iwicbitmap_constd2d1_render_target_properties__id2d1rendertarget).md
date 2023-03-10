---
UID: NF:d2d1.ID2D1Factory.CreateWicBitmapRenderTarget(IWICBitmap,constD2D1_RENDER_TARGET_PROPERTIES&,ID2D1RenderTarget)
title: ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget) (d2d1.h)
description: Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap. (overload 2/2)
helpviewer_keywords: ["CreateWicBitmapRenderTarget","CreateWicBitmapRenderTarget method [Direct2D]","CreateWicBitmapRenderTarget method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateWicBitmapRenderTarget method","ID2D1Factory.CreateWicBitmapRenderTarget","ID2D1Factory.CreateWicBitmapRenderTarget(IWICBitmap","const D2D1_RENDER_TARGET_PROPERTIES &","ID2D1RenderTarget)","ID2D1Factory::CreateWicBitmapRenderTarget","ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap","const D2D1_RENDER_TARGET_PROPERTIES &","ID2D1RenderTarget)","d2d1/ID2D1Factory::CreateWicBitmapRenderTarget","direct2d.ID2D1Factory_CreateWicBitmapRenderTarget_ptr_IWICBitmap_ref_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget"]
old-location: direct2d\ID2D1Factory_CreateWicBitmapRenderTarget_ptr_IWICBitmap_ref_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget.htm
tech.root: Direct2D
ms.assetid: 012950f5-d609-40e2-8f3e-cfcbf5e368cc
ms.date: 12/05/2018
ms.keywords: CreateWicBitmapRenderTarget, CreateWicBitmapRenderTarget method [Direct2D], CreateWicBitmapRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateWicBitmapRenderTarget method, ID2D1Factory.CreateWicBitmapRenderTarget, ID2D1Factory.CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget), ID2D1Factory::CreateWicBitmapRenderTarget, ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget), d2d1/ID2D1Factory::CreateWicBitmapRenderTarget, direct2d.ID2D1Factory_CreateWicBitmapRenderTarget_ptr_IWICBitmap_ref_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget
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
 - ID2D1Factory::CreateWicBitmapRenderTarget
 - d2d1/ID2D1Factory::CreateWicBitmapRenderTarget
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
 - ID2D1Factory.CreateWicBitmapRenderTarget
---

# ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget)


## -description

Creates a render target that renders to a Microsoft Windows Imaging Component (WIC)  bitmap.

## -parameters

### -param target [in]

Type: <b><a href="/windows/win32/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>*</b>

The bitmap that receives the rendering output of the render target.

### -param renderTargetProperties [ref]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a></b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering. For information about supported pixel formats, see  <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>.

### -param renderTarget [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the  <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> object created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

You must use <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_feature_level">D2D1_FEATURE_LEVEL_DEFAULT</a> for the <b>minLevel</b> member of the  <i>renderTargetProperties</i> parameter with this method.

Your application should create render targets once and hold onto them for the life of the application or until the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).

> [!NOTE]
> This method isn't supported on Windows Phone, and will fail when called on a device with error code 0x8899000b  (“There is no hardware rendering device available for this operation”). Because the Windows Phone Emulator supports WARP rendering,  this method will fail when called on the emulator with a different error code, 0x88982f80  (wincodec_err_unsupportedpixelformat).

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

