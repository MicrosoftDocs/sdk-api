---
UID: NF:d2d1.ID2D1Factory.CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget)
title: ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget)
author: windows-sdk-content
description: Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.
old-location: direct2d\ID2D1Factory_CreateWicBitmapRenderTarget_ptr_IWICBitmap_ptr_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget.htm
old-project: direct2d
ms.assetid: fddd7a14-1fb0-4372-8f3e-94b54fef9051
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateWicBitmapRenderTarget, CreateWicBitmapRenderTarget method [Direct2D], CreateWicBitmapRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateWicBitmapRenderTarget method, ID2D1Factory.CreateWicBitmapRenderTarget, ID2D1Factory.CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget), ID2D1Factory::CreateWicBitmapRenderTarget, ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget), d2d1/ID2D1Factory::CreateWicBitmapRenderTarget, direct2d.ID2D1Factory_CreateWicBitmapRenderTarget_ptr_IWICBitmap_ptr_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateWicBitmapRenderTarget
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ID2D1Factory::CreateWicBitmapRenderTarget(IWICBitmap,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget)


## -description


Creates a render target that renders to a Microsoft Windows Imaging Component (WIC)  bitmap.


## -parameters




### -param target [in]

Type: <b><a href="_wic_codec_iwicbitmap">IWICBitmap</a>*</b>

The bitmap that receives the rendering output of the render target.


### -param renderTargetProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering. For information about supported pixel formats, see  <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>.


### -param renderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> object created by this method. 


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must use <a href="https://msdn.microsoft.com/d9604c37-7345-40e3-850c-2e2c99353ba5">D2D1_FEATURE_LEVEL_DEFAULT</a> for the <b>minLevel</b> member of the  <i>renderTargetProperties</i> parameter with this method.

Your application should create render targets once and hold onto them for the life of the application or until the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).

<div class="os_icon_block">
<ul class="os_icon_images">
<li><img alt="Applies to Windows Phone" src="../common/phone.png"/></li>
</ul>
<div class="os_icon_content_block">
<b>Note</b>    This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b  (“There is no hardware rendering device available for this operation”). Because the Windows Phone Emulator supports WARP rendering,  this method will fail when called on the emulator with a different error code, 0x88982f80  (wincodec_err_unsupportedpixelformat).

</div>
</div>



## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

