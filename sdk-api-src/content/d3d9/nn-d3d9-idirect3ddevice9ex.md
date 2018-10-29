---
UID: NN:d3d9.IDirect3DDevice9Ex
title: IDirect3DDevice9Ex
author: windows-sdk-content
description: Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
old-location: direct3d9\idirect3ddevice9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 6755c62f-1ee8-9783-0c97-7e582de29a4b, IDirect3DDevice9Ex, IDirect3DDevice9Ex interface [Direct3D 9], IDirect3DDevice9Ex interface [Direct3D 9],described, d3d9/IDirect3DDevice9Ex, direct3d9.idirect3ddevice9ex
ms.prod: windows
ms.technology: windows-sdk
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


Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. The IDirect3DDevice9Ex interface derives from the <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9Ex</b> interface inherits from <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>. <b>IDirect3DDevice9Ex</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">CheckDeviceState</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd8a5992-f50a-403b-8645-87e8473a3538">CheckResourceResidency</a>
</td>
<td align="left" width="63%">
Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fd99d5b-0b54-43d8-9f94-1f8c14e98e69">ComposeRects</a>
</td>
<td align="left" width="63%">
Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29227080-0ddc-4297-b470-8849ec84fa47">CreateDepthStencilSurfaceEx</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03fd24f4-9db2-4763-b7c7-85c6d05c3c77">CreateOffscreenPlainSurfaceEx</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b928448-a212-41e2-b81b-b8a5f9a1d848">CreateRenderTargetEx</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa5b08f7-abb0-4f59-8454-4016cb029f1e">GetDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724a4512-b40d-427f-964f-9f0988ebbe26">GetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Get the priority of the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3acb0675-e20a-4ecd-8f29-3867051acb26">GetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames of data that the system is allowed to queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">PresentEx</a>
</td>
<td align="left" width="63%">
Swap the swapchain's next buffer with the front buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03c8084e-eff1-4c01-9102-f7fb777585a4">ResetEx</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain with all other surfaces persistent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2576f38-c2c9-41a0-a680-3eb8c3015f8a">SetConvolutionMonoKernel</a>
</td>
<td align="left" width="63%">
Prepare the texture sampler for monochrome convolution filtering on a single-color texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa9dd95e-74ce-4f48-bd60-8cabc2013377">SetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Set the priority on the GPU thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a6606b6-336d-4e13-bac4-8bd8c770b1d8">SetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Set the number of frames that the system is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45f41a97-ab2f-4e90-aeb7-06de86fcbd72">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  
<a href="https://msdn.microsoft.com/45f41a97-ab2f-4e90-aeb7-06de86fcbd72">TestCooperativeLevel</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">CheckDeviceState</a>.</div>
<div> </div>
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3c329c8-30fa-4e39-8cd5-27130531f2ce">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Suspend execution of the calling thread until the next vertical blank signal.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DDevice9Ex</b> interface is obtained by calling <a href="https://msdn.microsoft.com/7182c5ea-40ca-4cf8-a33e-b22984fc9349">IDirect3D9Ex::CreateDeviceEx</a>.

The LPDIRECT3DDEVICE9EX and PDIRECT3DDEVICE9EX types are defined as pointers to the IDirect3DDevice9Ex interface:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DDevice9Ex *LPDIRECT3DDEVICE9EX, *PDIRECT3DDEVICE9EX;
</pre>
</td>
</tr>
</table></span></div>


<h3><a id="Creating_a_Device"></a><a id="creating_a_device"></a><a id="CREATING_A_DEVICE"></a>Creating a Device</h3>
Follow these two steps to initialize a Direct3D device:

<ol>
<li>Call <a href="https://msdn.microsoft.com/5480ecab-9820-4352-9587-4eba6ab26ebf">Direct3DCreate9Ex</a> to create the Direct3D object.</li>
<li>Call <a href="https://msdn.microsoft.com/7182c5ea-40ca-4cf8-a33e-b22984fc9349">CreateDeviceEx</a> to create the Direct3D device.</li>
</ol>
Here is an example:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDirect3D9Ex *pDirect3DEx;
LPDIRECT3DDEVICE9EX pDeviceEx;
DWORD behaviorFlags = D3DCREATE_HARDWARE_VERTEXPROCESSING;

Direct3DCreate9Ex(D3D_SDK_VERSION, &amp;pDirect3DEx);
pDirect3DEx-&gt;CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd, behaviorFlags, &amp;d3dpp, NULL, &amp;pDeviceEx);
</pre>
</td>
</tr>
</table></span></div>





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

