---
UID: NF:d2d1.ID2D1RenderTarget.CreateSharedBitmap
title: ID2D1RenderTarget::CreateSharedBitmap
author: windows-sdk-content
description: Creates an ID2D1Bitmap whose data is shared with another resource.
old-location: direct2d\ID2D1RenderTarget_CreateSharedBitmap.htm
tech.root: direct2d
ms.assetid: c6377dbd-ffd9-458b-9e03-5a832f095818
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateSharedBitmap, CreateSharedBitmap method [Direct2D], CreateSharedBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateSharedBitmap method, ID2D1RenderTarget.CreateSharedBitmap, ID2D1RenderTarget::CreateSharedBitmap, d2d1/ID2D1RenderTarget::CreateSharedBitmap, direct2d.ID2D1RenderTarget_CreateSharedBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.CreateSharedBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateSharedBitmap


## -description


Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> whose data is shared with another resource.


## -parameters




### -param riid

Type: <b>REFIID</b>

The interface ID of the object supplying the source data.


### -param data [in, out]

Type: <b>void*</b>

An <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>, <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a>, or an <a href="_wic_codec_iwicbitmaplock">IWICBitmapLock</a> that contains the data to share with the new <b>ID2D1Bitmap</b>. For more information, see the Remarks section.


### -param bitmapProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/050246fd-f91a-4a2a-858a-5f0447e3ecbf">D2D1_BITMAP_PROPERTIES</a>*</b>

The pixel format  and DPI of the bitmap to create . The <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT</a> portion of the pixel format  must match the <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT</a> of <i>data</i> or the method will fail, but the alpha modes don't have to match. To prevent a  mismatch, you can pass <b>NULL</b> or the value obtained from the <a href="https://msdn.microsoft.com/97128e07-68c2-40ab-bad1-7b6f599291b9">D2D1::PixelFormat</a> helper function. The DPI settings do not have to match those of <i>data</i>. If both <i>dpiX</i> and <i>dpiY</i> are  0.0f, the DPI of the render target is used.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>**</b>

When this method returns, contains the address of a pointer to the new bitmap. This parameter is passed uninitialized. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>CreateSharedBitmap</b> method is useful for efficiently reusing bitmap data and can also be used to provide interoperability with Direct3D. 

<h3><a id="Sharing_an_ID2D1Bitmap"></a><a id="sharing_an_id2d1bitmap"></a><a id="SHARING_AN_ID2D1BITMAP"></a>Sharing an ID2D1Bitmap</h3>
By passing an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> created by a render target that is resource-compatible, you can share a bitmap with that render target; both the original <b>ID2D1Bitmap</b> and the new <b>ID2D1Bitmap</b> created by this method will point to the same bitmap data. For more information about when render target resources can be shared, see the Sharing Render Target Resources section of the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.

You may also use this method to reinterpret the data of an existing bitmap and specify a new DPI or alpha mode. For example, in the case of a bitmap atlas, an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> may contain multiple sub-images, each of which should be rendered with a different <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a> (<b>D2D1_ALPHA_MODE_PREMULTIPLIED</b>  or <b>D2D1_ALPHA_MODE_IGNORE</b>). You could use the <b>CreateSharedBitmap</b> method to reinterpret the bitmap using the desired alpha mode  without having to load a separate copy of the bitmap into memory.

<h3><a id="Sharing_an_IDXGISurface"></a><a id="sharing_an_idxgisurface"></a><a id="SHARING_AN_IDXGISURFACE"></a>Sharing an IDXGISurface</h3>
When using a DXGI surface render target (an <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> object created by the <a href="https://msdn.microsoft.com/101744ea-97bc-4f92-88b0-fcdf0e4aaf4e">CreateDxgiSurfaceRenderTarget</a> method), you can pass an  <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a> surface to the <b>CreateSharedBitmap</b> method to share video memory with Direct3D and manipulate Direct3D content as an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>. As described in  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>, the render target and the <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a> must be using the same Direct3D device. 

Note also that the <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a> must use one of the supported pixel formats and alpha modes described in <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.

For more information about interoperability with Direct3D, see the <a href="https://msdn.microsoft.com/27680714-dc68-44eb-ab16-2cae3529b352">Direct2D and Direct3D Interoperability Overview</a>.

<h3><a id="Sharing_an_IWICBitmapLock"></a><a id="sharing_an_iwicbitmaplock"></a><a id="SHARING_AN_IWICBITMAPLOCK"></a>Sharing an IWICBitmapLock</h3>
An <a href="_wic_codec_iwicbitmaplock">IWICBitmapLock</a> stores the content of a WIC bitmap and shields it from simultaneous accesses. By passing an <b>IWICBitmapLock</b>  to the <b>CreateSharedBitmap</b> method, you can create an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> that points to the bitmap data already stored in the  <b>IWICBitmapLock</b>. 

To use an <a href="_wic_codec_iwicbitmaplock">IWICBitmapLock</a> with the <b>CreateSharedBitmap</b> method, the render target must use software rendering. To force a render target to use software rendering, set to <a href="https://msdn.microsoft.com/4ae6e4cf-e1c9-476e-a7b5-31cdad9cf321">D2D1_RENDER_TARGET_TYPE_SOFTWARE</a>  the <b>type</b> field of the  <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a> structure that you use to create the render target. To check whether an existing render target uses software rendering, use the <a href="https://msdn.microsoft.com/d9fbc313-fe82-4425-9c9a-79bfacc08019">IsSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/27680714-dc68-44eb-ab16-2cae3529b352">Direct2D and Direct3D Interoperability Overview</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a>



<a href="_wic_codec_iwicbitmaplock">IWICBitmapLock</a>



<a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

