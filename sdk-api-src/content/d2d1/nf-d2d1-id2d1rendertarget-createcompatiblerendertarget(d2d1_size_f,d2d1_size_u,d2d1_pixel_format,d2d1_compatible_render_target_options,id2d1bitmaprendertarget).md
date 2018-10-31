---
UID: NF:d2d1.ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget)
title: ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget)
author: windows-sdk-content
description: Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.
old-location: direct2d\ID2D1RenderTarget_CreateCompatibleRenderTarget_overload6.htm
tech.root: direct2d
ms.assetid: 043d18f4-0cf6-47eb-9a1e-aa676a947bd6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateCompatibleRenderTarget, CreateCompatibleRenderTarget method [Direct2D], CreateCompatibleRenderTarget method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateCompatibleRenderTarget method, ID2D1RenderTarget.CreateCompatibleRenderTarget, ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget), ID2D1RenderTarget::CreateCompatibleRenderTarget, ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget), d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_D2D_SIZE_F_D2D_SIZE_U_D2D1_PIXEL_FORMAT_D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_ptr_ptr_ID2D1BitmapRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload6
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
 - ID2D1RenderTarget.CreateCompatibleRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget)


## -description


Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.


## -parameters




### -param desiredSize

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The desired size of the new render target in device-independent pixels if it should be different from the original render target. For more information, see the Remarks section.


### -param desiredPixelSize

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The desired size of the new render target in pixels if it should be different from the original render target. For more information, see the Remarks section.


### -param desiredFormat

Type: <b><a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a></b>

The desired pixel format and alpha mode of the new render target. If the pixel format is set to DXGI_FORMAT_UNKNOWN, the new render target uses the same pixel format as the original render target. If the alpha mode is <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_UNKNOWN</a>, the alpha mode of the new render target defaults to <b>D2D1_ALPHA_MODE_PREMULTIPLIED</b>. For information about supported pixel formats, see  <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>.


### -param options

Type: <b><a href="https://msdn.microsoft.com/c20bf016-2304-4bd3-88ad-42d81e69c302">D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS</a></b>

A value that specifies whether the new render target must be compatible with GDI.


### -param bitmapRenderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a>**</b>

When this method returns, contains a pointer to a pointer to a new bitmap render target. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The pixel size and DPI of the new render target can be altered by specifying values for <i>desiredSize</i> or <i>desiredPixelSize</i>:  

<ul>
<li>If <i>desiredSize</i> is specified but <i>desiredPixelSize</i> is not, the pixel size is computed from the desired size using the parent target DPI. If the <i>desiredSize</i> maps to a integer-pixel size, the DPI of the compatible render target is the same as the DPI of the parent target.  If <i>desiredSize</i> maps to a fractional-pixel size, the pixel size is rounded up to the nearest integer and the DPI for the compatible render target is slightly higher than the DPI of the parent render target. In all cases, the coordinate (<i>desiredSize</i>.width, <i>desiredSize</i>.height) maps to the lower-right corner of the compatible render target.</li>
<li>If the <i>desiredPixelSize</i> is specified and <i>desiredSize</i>  is not, the DPI of the new render target is the same as the original render target.</li>
<li>If both <i>desiredSize</i>  and <i>desiredPixelSize</i> are specified, the DPI of the new render target is computed to account for the difference in scale.</li>
<li>If neither <i>desiredSize</i> nor <i>desiredPixelSize</i> is specified, the new render target size and DPI match the original render target. </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

