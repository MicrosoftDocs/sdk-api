---
UID: NN:d3d9.IDirect3DDevice9Ex
title: IDirect3DDevice9Ex (d3d9.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
old-location: direct3d9\idirect3ddevice9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6755c62f-1ee8-9783-0c97-7e582de29a4b, IDirect3DDevice9Ex, IDirect3DDevice9Ex interface [Direct3D 9], IDirect3DDevice9Ex interface [Direct3D 9],described, d3d9/IDirect3DDevice9Ex, direct3d9.idirect3ddevice9ex
ms.topic: interface
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex interface


## -description


Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. The IDirect3DDevice9Ex interface derives from the <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9Ex</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>. <b>IDirect3DDevice9Ex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDevice9Ex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174338(v=VS.85).aspx">CheckDeviceState</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174339(v=VS.85).aspx">CheckResourceResidency</a>
</td>
<td align="left" width="63%">
Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174340(v=VS.85).aspx">ComposeRects</a>
</td>
<td align="left" width="63%">
Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb509711(v=VS.85).aspx">CreateDepthStencilSurfaceEx</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb509712(v=VS.85).aspx">CreateOffscreenPlainSurfaceEx</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb509713(v=VS.85).aspx">CreateRenderTargetEx</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb509714(v=VS.85).aspx">GetDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174341(v=VS.85).aspx">GetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Get the priority of the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174342(v=VS.85).aspx">GetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames of data that the system is allowed to queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174343(v=VS.85).aspx">PresentEx</a>
</td>
<td align="left" width="63%">
Swap the swapchain's next buffer with the front buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174344(v=VS.85).aspx">ResetEx</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain with all other surfaces persistent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174345(v=VS.85).aspx">SetConvolutionMonoKernel</a>
</td>
<td align="left" width="63%">
Prepare the texture sampler for monochrome convolution filtering on a single-color texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174346(v=VS.85).aspx">SetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Set the priority on the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174347(v=VS.85).aspx">SetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Set the number of frames that the system is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174348(v=VS.85).aspx">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  
<a href="https://msdn.microsoft.com/en-us/library/Bb174348(v=VS.85).aspx">TestCooperativeLevel</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Bb174338(v=VS.85).aspx">CheckDeviceState</a>.</div>
<div> </div>
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174349(v=VS.85).aspx">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Suspend execution of the calling thread until the next vertical blank signal.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DDevice9Ex</b> interface is obtained by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174302(v=VS.85).aspx">IDirect3D9Ex::CreateDeviceEx</a>.

The LPDIRECT3DDEVICE9EX and PDIRECT3DDEVICE9EX types are defined as pointers to the IDirect3DDevice9Ex interface:



```

typedef struct IDirect3DDevice9Ex *LPDIRECT3DDEVICE9EX, *PDIRECT3DDEVICE9EX;

```




<h3><a id="Creating_a_Device"></a><a id="creating_a_device"></a><a id="CREATING_A_DEVICE"></a>Creating a Device</h3>
Follow these two steps to initialize a Direct3D device:

<ol>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Bb219676(v=VS.85).aspx">Direct3DCreate9Ex</a> to create the Direct3D object.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Bb174302(v=VS.85).aspx">CreateDeviceEx</a> to create the Direct3D device.</li>
</ol>
Here is an example:



```

IDirect3D9Ex *pDirect3DEx;
LPDIRECT3DDEVICE9EX pDeviceEx;
DWORD behaviorFlags = D3DCREATE_HARDWARE_VERTEXPROCESSING;

Direct3DCreate9Ex(D3D_SDK_VERSION, &pDirect3DEx);
pDirect3DEx->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd, behaviorFlags, &d3dpp, NULL, &pDeviceEx);

```







## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

