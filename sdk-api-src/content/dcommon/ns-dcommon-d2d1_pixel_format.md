---
UID: NS:dcommon.D2D1_PIXEL_FORMAT
title: D2D1_PIXEL_FORMAT
author: windows-sdk-content
description: Contains the data format and alpha mode for a bitmap or render target.
old-location: direct2d\D2D1_PIXEL_FORMAT.htm
old-project: direct2d
ms.assetid: e95afd9c-5793-4cb7-bcb8-aae4d28b6532
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: D2D1_PIXEL_FORMAT, D2D1_PIXEL_FORMAT structure [Direct2D], dcommon/D2D1_PIXEL_FORMAT, direct2d.D2D1_PIXEL_FORMAT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dcommon.h
req.include-header: D2d1.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: D2D1_PIXEL_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcommon.h
api_name:
 - D2D1_PIXEL_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_PIXEL_FORMAT structure


## -description



    Contains the data format and alpha mode for a bitmap or render target. 


## -struct-fields




### -field format

Type: <b><a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT</a></b>

A value that specifies the size and arrangement of channels in each pixel.


### -field alphaMode

Type: <b><a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a></b>

A value that specifies whether the alpha channel is using pre-multiplied alpha, straight alpha, whether it should be ignored and considered opaque, or whether it is unkown.  


## -remarks



For more information about the pixel formats and alpha modes supported by each render target, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.


#### Examples

The following example creates a <b>D2D1_PIXEL_FORMAT</b> structure and uses it to specify the pixel format and alpha mode of an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>RECT rc;
GetClientRect(m_hwnd, &amp;rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory-&gt;CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &amp;m_pRT
    );

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/97128e07-68c2-40ab-bad1-7b6f599291b9">D2D1::PixelFormat</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

