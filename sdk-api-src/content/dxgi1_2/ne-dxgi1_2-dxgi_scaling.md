---
UID: NE:dxgi1_2.DXGI_SCALING
title: DXGI_SCALING
author: windows-sdk-content
description: Identifies resize behavior when the back-buffer size does not match the size of the target output.
old-location: direct3ddxgi\dxgi_scaling.htm
tech.root: direct3ddxgi
ms.assetid: 7EEA4B02-3C81-4A07-BE3B-80A5E35A16BE
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DXGI_SCALING, DXGI_SCALING enumeration [DXGI], DXGI_SCALING_ASPECT_RATIO_STRETCH, DXGI_SCALING_NONE, DXGI_SCALING_STRETCH, direct3ddxgi.dxgi_scaling, dxgi1_2/DXGI_SCALING, dxgi1_2/DXGI_SCALING_ASPECT_RATIO_STRETCH, dxgi1_2/DXGI_SCALING_NONE, dxgi1_2/DXGI_SCALING_STRETCH
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dxgi1_2.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_SCALING
product: Windows
targetos: Windows
req.typenames: DXGI_SCALING
req.redist: 
---

# DXGI_SCALING enumeration


## -description


Identifies resize behavior when the back-buffer size does not match the size of the target output.


## -enum-fields




### -field DXGI_SCALING_STRETCH

Directs DXGI to make the back-buffer contents scale to fit the presentation target size. This is the implicit behavior of DXGI when you call the <a href="https://msdn.microsoft.com/en-us/library/Bb174537(v=VS.85).aspx">IDXGIFactory::CreateSwapChain</a> method.


### -field DXGI_SCALING_NONE

Directs DXGI to make the back-buffer contents appear without any scaling when the presentation target size is not equal to the back-buffer size. The top edges of the back buffer and presentation target are aligned together. If the WS_EX_LAYOUTRTL style is associated with the <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> handle to the target output window, the right edges of the back buffer and presentation target are aligned together; otherwise, the left edges are aligned together. All target area outside the back buffer is filled with window background color.

This value specifies that all target areas outside the back buffer of a swap chain are filled with the background color that you specify in a call to <a href="https://msdn.microsoft.com/E46CA219-303F-40D4-8C62-6241C9199BA0">IDXGISwapChain1::SetBackgroundColor</a>.


### -field DXGI_SCALING_ASPECT_RATIO_STRETCH

Directs DXGI to make the back-buffer contents scale to fit the presentation target size, while preserving the aspect ratio of the back-buffer. If the scaled back-buffer does not fill the presentation area, it will be centered with black borders.

This constant is supported on Windows Phone 8 and Windows 10. 

Note that with legacy Win32 window swapchains, this works the same as DXGI_SCALING_STRETCH.



## -remarks



The DXGI_SCALING_NONE value is supported only for flip presentation model swap chains that you create with the <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value. You pass these values in a call to <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or  <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>. 

DXGI_SCALING_ASPECT_RATIO_STRETCH will prefer to use a horizontal fill, otherwise it will use a vertical fill, using the following logic.

<pre class="syntax" xml:space="preserve"><code>float aspectRatio = backBufferWidth / float(backBufferHeight);

 // Horizontal fill
 float scaledWidth = outputWidth;
 float scaledHeight = outputWidth / aspectRatio;
 if (scaledHeight &gt;= outputHeight)
 {
   // Do vertical fill
   scaledWidth = outputHeight * aspectRatio;
   scaledHeight = outputHeight;
 }

 float offsetX = (outputWidth - scaledWidth) * 0.5f;
 float offsetY = (outputHeight - scaledHeight) * 0.5f;

 rect.left = static_cast&lt;LONG&gt;(offsetX);
 rect.top = static_cast&lt;LONG&gt;(offsetY);
 rect.right = static_cast&lt;LONG&gt;(offsetX + scaledWidth);
 rect.bottom = static_cast&lt;LONG&gt;(offsetY + scaledHeight);

 rect.left = std::max&lt;LONG&gt;(0, rect.left);
 rect.top = std::max&lt;LONG&gt;(0, rect.top);
 rect.right = std::min&lt;LONG&gt;(static_cast&lt;LONG&gt;(outputWidth), rect.right);
 rect.bottom = std::min&lt;LONG&gt;(static_cast&lt;LONG&gt;(outputHeight), rect.bottom);
</code></pre>
Note that <i>outputWidth</i> and <i>outputHeight</i> are the pixel sizes of the presentation target size. In the case of <b>CoreWindow</b>, this requires converting the <i>logicalWidth</i> and <i>logicalHeight</i> values from DIPS to pixels using the window's DPI property.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a>
 

 

