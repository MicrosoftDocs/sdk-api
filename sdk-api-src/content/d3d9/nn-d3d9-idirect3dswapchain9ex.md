---
UID: NN:d3d9.IDirect3DSwapChain9Ex
title: IDirect3DSwapChain9Ex (d3d9.h)
description: Applications use the methods of the IDirect3DSwapChain9Ex interface to manipulate a swap chain.
helpviewer_keywords: ["5cc4ce3b-e2da-a3fd-de25-b60e0d8d1030","IDirect3DSwapChain9Ex","IDirect3DSwapChain9Ex interface [Direct3D 9]","IDirect3DSwapChain9Ex interface [Direct3D 9]","described","d3d9/IDirect3DSwapChain9Ex","direct3d9.d3d9l_idirect3dswapchain9"]
old-location: direct3d9\d3d9l_idirect3dswapchain9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\d3d9l_idirect3dswapchain9.htm
ms.date: 12/05/2018
ms.keywords: 5cc4ce3b-e2da-a3fd-de25-b60e0d8d1030, IDirect3DSwapChain9Ex, IDirect3DSwapChain9Ex interface [Direct3D 9], IDirect3DSwapChain9Ex interface [Direct3D 9],described, d3d9/IDirect3DSwapChain9Ex, direct3d9.d3d9l_idirect3dswapchain9
f1_keywords:
- d3d9/IDirect3DSwapChain9Ex
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
- IDirect3DSwapChain9Ex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DSwapChain9Ex interface


## -description


Applications use the methods of the <b>IDirect3DSwapChain9Ex</b> interface to manipulate a swap chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DSwapChain9Ex</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>. <b>IDirect3DSwapChain9Ex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DSwapChain9Ex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex">GetDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount">GetLastPresentCount</a>
</td>
<td align="left" width="63%">
Returns the number of times the swapchain has been processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)">GetPresentStatistics</a>
</td>
<td align="left" width="63%">
Gets presentation statistics so an application can identify frames that do not have a Present method call.

</td>
</tr>
</table> 


## -remarks



There is always at least one swap chain for each device, known as the implicit swap chain. However, an additional swap chain for rendering multiple views from the same device can be created by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">CreateAdditionalSwapChain</a> method.

This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The <b>LPDIRECT3DSWAPCHAIN9</b> and <b>PDIRECT3DSWAPCHAIN9</b> types are defined as pointers to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a> interface.

<b>IDirect3DSwapChain9Ex</b> objects are returned as a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a> object when <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getswapchain">GetSwapChain</a> is called on an instance of <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>.
The <b>IDirect3DSwapChain9Ex</b> interface is obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the instance of <b>IDirect3DSwapChain9</b> that was returned by <b>GetSwapChain</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9lh">Feature Summary (Direct3D 9 for Windows Vista)</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>
 

 

