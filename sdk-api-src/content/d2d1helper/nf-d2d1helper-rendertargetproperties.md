---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# RenderTargetProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a> structure.


## -parameters




### -param type

Type: <b><a href="https://msdn.microsoft.com/4ae6e4cf-e1c9-476e-a7b5-31cdad9cf321">D2D1_RENDER_TARGET_TYPE</a></b>

A value that specifies whether the render target must use hardware rendering or software rendering. The default value, <a href="https://msdn.microsoft.com/4ae6e4cf-e1c9-476e-a7b5-31cdad9cf321">D2D1_RENDER_TARGET_TYPE_DEFAULT</a>, specifies that hardware rendering be used; if hardware rendering is not available, the render target uses software rendering. Note that WIC bitmap render targets do not support hardware rendering.


### -param pixelFormat [in]

Type: <b>const <a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a></b>

The pixel format and alpha mode of the render target. The default pixel format is <a href="https://msdn.microsoft.com/97128e07-68c2-40ab-bad1-7b6f599291b9">D2D1::PixelFormat</a>, which tells Direct2D to select a pixel format that is supported by the render target.  For a list of pixel formats and alpha modes supported by each render target, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.


### -param dpiX

Type: <b>FLOAT</b>

The horizontal DPI of the render target. The default value is 0.0. If both <i>dpiX</i> and <i>dpiY</i> are set to 0.0, the render target uses its default DPI.  For more information, see <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>.


### -param dpiY

Type: <b>FLOAT</b>

The vertical DPI of the render target. The default value is 0.0. If both <i>dpiX</i> and <i>dpiY</i> are set to 0.0, the render target uses its default DPI. For more information, see <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>. 


### -param usage

Type: <b><a href="https://msdn.microsoft.com/12d717c4-5f81-4bbf-a693-042e51913081">D2D1_RENDER_TARGET_USAGE</a></b>

Specifies how the render target is remotely rendered and whether it should be GDI-compatible.  The default value, <a href="https://msdn.microsoft.com/12d717c4-5f81-4bbf-a693-042e51913081">D2D1_RENDER_TARGET_USAGE_NONE</a>, creates a render target that is not compatible with GDI and that uses Direct3D command-stream remote rendering, if it is available. 


### -param minLevel

Type: <b><a href="https://msdn.microsoft.com/d9604c37-7345-40e3-850c-2e2c99353ba5">D2D1_FEATURE_LEVEL</a></b>

The minimum Direct3D feature level that is required for hardware rendering. The default value, <a href="https://msdn.microsoft.com/d9604c37-7345-40e3-850c-2e2c99353ba5">D2D1_FEATURE_LEVEL_DEFAULT</a>, indicates that Direct2D should determine whether the Direct3D feature level of the device is adequate. This field is used only when <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a> and <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a> objects are created.  For more information, see <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a></b>

A <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a> that contains the specified settings. 




## -see-also




<a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES Structure</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

