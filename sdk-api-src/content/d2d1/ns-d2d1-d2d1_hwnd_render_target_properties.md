---
UID: NS:d2d1.D2D1_HWND_RENDER_TARGET_PROPERTIES
title: D2D1_HWND_RENDER_TARGET_PROPERTIES
author: windows-sdk-content
description: Contains the HWND, pixel size, and presentation options for an ID2D1HwndRenderTarget.
old-location: direct2d\D2D1_HWND_RENDER_TARGET_PROPERTIES.htm
tech.root: direct2d
ms.assetid: 4300843a-a24f-4f9e-a396-67172f083638
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D2D1_HWND_RENDER_TARGET_PROPERTIES, D2D1_HWND_RENDER_TARGET_PROPERTIES structure [Direct2D], d2d1/D2D1_HWND_RENDER_TARGET_PROPERTIES, direct2d.D2D1_HWND_RENDER_TARGET_PROPERTIES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_HWND_RENDER_TARGET_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_HWND_RENDER_TARGET_PROPERTIES
req.redist: 
---

# D2D1_HWND_RENDER_TARGET_PROPERTIES structure


## -description


Contains the HWND, pixel size, and presentation options for an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>.


## -struct-fields




### -field hwnd

Type: <b>HWND</b>

The HWND to which the render target issues the output from its drawing commands.


### -field pixelSize

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The size of the render target, in pixels.


### -field presentOptions

Type: <b><a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS</a></b>

A value that specifies whether the render target retains the frame after it is presented and whether the render target waits for the device to refresh before presenting.


## -remarks



Use this structure when you call the <a href="https://msdn.microsoft.com/3b55b1b0-a423-40dc-9581-c1fbe8134ca5">CreateHwndRenderTarget</a> method to create a new <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>.

For convenience, Direct2D provides the <a href="https://msdn.microsoft.com/41d4c58d-6840-48b6-8e31-1a0c412156cb">D2D1::HwndRenderTargetProperties</a> function for creating new <b>D2D1_HWND_RENDER_TARGET_PROPERTIES</b> structures.


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/3b55b1b0-a423-40dc-9581-c1fbe8134ca5">CreateHwndRenderTarget</a> method to create an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>. It uses the <a href="https://msdn.microsoft.com/41d4c58d-6840-48b6-8e31-1a0c412156cb">D2D1::HwndRenderTargetProperties</a> helper function to create a <b>D2D1_HWND_RENDER_TARGET_PROPERTIES</b> structure that contains a handle to a window and the size of the drawing area. Because a <a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS</a> value isn't specified, the function uses the default value, <b>D2D1_PRESENT_OPTIONS_NONE</b>.  

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

// Create a Direct2D render target.
hr = m_pD2DFactory-&gt;CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &amp;m_pRenderTarget
    );
</pre>
</td>
</tr>
</table></span></div>
Code has been omitted from this example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>
 

 

