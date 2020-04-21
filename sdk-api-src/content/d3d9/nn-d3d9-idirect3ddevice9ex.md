---
UID: NN:d3d9.IDirect3DDevice9Ex
title: IDirect3DDevice9Ex (d3d9.h)
description: Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.helpviewer_keywords: ["6755c62f-1ee8-9783-0c97-7e582de29a4b","IDirect3DDevice9Ex","IDirect3DDevice9Ex interface [Direct3D 9]","IDirect3DDevice9Ex interface [Direct3D 9]","described","d3d9/IDirect3DDevice9Ex","direct3d9.idirect3ddevice9ex"]
old-location: direct3d9\idirect3ddevice9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex.htm
ms.date: 12/05/2018
ms.keywords: 6755c62f-1ee8-9783-0c97-7e582de29a4b, IDirect3DDevice9Ex, IDirect3DDevice9Ex interface [Direct3D 9], IDirect3DDevice9Ex interface [Direct3D 9],described, d3d9/IDirect3DDevice9Ex, direct3d9.idirect3ddevice9ex
f1_keywords:
- d3d9/IDirect3DDevice9Ex
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9Ex interface


## -description


Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. The IDirect3DDevice9Ex interface derives from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9Ex</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>. <b>IDirect3DDevice9Ex</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">CheckDeviceState</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkresourceresidency">CheckResourceResidency</a>
</td>
<td align="left" width="63%">
Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects">ComposeRects</a>
</td>
<td align="left" width="63%">
Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex">CreateDepthStencilSurfaceEx</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex">CreateOffscreenPlainSurfaceEx</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex">CreateRenderTargetEx</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex">GetDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getgputhreadpriority">GetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Get the priority of the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getmaximumframelatency">GetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames of data that the system is allowed to queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">PresentEx</a>
</td>
<td align="left" width="63%">
Swap the swapchain's next buffer with the front buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex">ResetEx</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain with all other surfaces persistent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel">SetConvolutionMonoKernel</a>
</td>
<td align="left" width="63%">
Prepare the texture sampler for monochrome convolution filtering on a single-color texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setgputhreadpriority">SetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Set the priority on the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setmaximumframelatency">SetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Set the number of frames that the system is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-testcooperativelevel">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-testcooperativelevel">TestCooperativeLevel</a> is no longer available for use. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">CheckDeviceState</a>.</div>
<div> </div>
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-waitforvblank">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Suspend execution of the calling thread until the next vertical blank signal.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DDevice9Ex</b> interface is obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex">IDirect3D9Ex::CreateDeviceEx</a>.

The LPDIRECT3DDEVICE9EX and PDIRECT3DDEVICE9EX types are defined as pointers to the IDirect3DDevice9Ex interface:



```

typedef struct IDirect3DDevice9Ex *LPDIRECT3DDEVICE9EX, *PDIRECT3DDEVICE9EX;

```




<h3><a id="Creating_a_Device"></a><a id="creating_a_device"></a><a id="CREATING_A_DEVICE"></a>Creating a Device</h3>
Follow these two steps to initialize a Direct3D device:

<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-direct3dcreate9ex">Direct3DCreate9Ex</a> to create the Direct3D object.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex">CreateDeviceEx</a> to create the Direct3D device.</li>
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




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
 

 

