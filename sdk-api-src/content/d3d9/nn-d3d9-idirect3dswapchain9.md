---
UID: NN:d3d9.IDirect3DSwapChain9
title: IDirect3DSwapChain9
author: windows-driver-content
description: Applications use the methods of the IDirect3DSwapChain9 interface to manipulate a swap chain.
old-location: direct3d9\idirect3dswapchain9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 9b1ef0f9-2688-f6ec-ae04-d0dc94b7d8b9, IDirect3DSwapChain9, IDirect3DSwapChain9 interface [Direct3D 9], IDirect3DSwapChain9 interface [Direct3D 9], described, d3d9helper/IDirect3DSwapChain9, direct3d9.idirect3dswapchain9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d9.lib
-	d3d9.dll
api_name:
-	IDirect3DSwapChain9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DSwapChain9 interface


## -description


Applications use the methods of the IDirect3DSwapChain9 interface to manipulate a swap chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DSwapChain9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DSwapChain9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DSwapChain9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89fa363f-023d-43aa-8f09-fa80ac49ccb6">GetBackBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a back buffer from the swap chain of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccef372e-7efa-44d0-b07c-21e894726f23">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f5782b9-b648-494d-9304-4df0a88476eb">GetFrontBufferData</a>
</td>
<td align="left" width="63%">
Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c85259-d958-4256-9327-67ade7c5581a">GetPresentParameters</a>
</td>
<td align="left" width="63%">
Retrieves the presentation parameters associated with a swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn940224">GetRasterStatus</a>
</td>
<td align="left" width="63%">
Returns information describing the raster of the monitor on which the swap chain is presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac90aee6-dd66-46d8-a628-4bf8bff087b4">Present</a>
</td>
<td align="left" width="63%">
Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain.

</td>
</tr>
</table> 


## -remarks



There is always at least one swap chain for each device, known as the implicit swap chain. However, an additional swap chain for rendering multiple views from the same device can be created by calling the <a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">IDirect3DDevice9::CreateAdditionalSwapChain</a> method.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DSWAPCHAIN9 and PDIRECT3DSWAPCHAIN9 types are defined as pointers to the <b>IDirect3DSwapChain9</b> interface. 
    




<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DSwapChain9 *LPDIRECT3DSWAPCHAIN9, *PDIRECT3DSWAPCHAIN9;
</pre>
</td>
</tr>
</table></span></div>
Note the application should ensure that its associated device window is visible when its swapchain(s) is in fullscreen mode. Invisible windows cannot receive user mode events and invisible fullscreen windows will interfere with other windowed mode applications' presentation.




## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">IDirect3DDevice9::CreateAdditionalSwapChain</a>
 

 

