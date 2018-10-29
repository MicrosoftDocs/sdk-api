---
UID: NN:d3d9.IDirect3DSwapChain9Ex
title: IDirect3DSwapChain9Ex
author: windows-sdk-content
description: Applications use the methods of the IDirect3DSwapChain9Ex interface to manipulate a swap chain.
old-location: direct3d9\d3d9l_idirect3dswapchain9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\d3d9l_idirect3dswapchain9.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 5cc4ce3b-e2da-a3fd-de25-b60e0d8d1030, IDirect3DSwapChain9Ex, IDirect3DSwapChain9Ex interface [Direct3D 9], IDirect3DSwapChain9Ex interface [Direct3D 9],described, d3d9/IDirect3DSwapChain9Ex, direct3d9.d3d9l_idirect3dswapchain9
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
 - IDirect3DSwapChain9Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSwapChain9Ex interface


## -description


Applications use the methods of the <b>IDirect3DSwapChain9Ex</b> interface to manipulate a swap chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DSwapChain9Ex</b> interface inherits from <a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>. <b>IDirect3DSwapChain9Ex</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e0e37c67-941c-4153-8b69-edf2d640b96d">GetDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16a101a5-d2c7-4fde-8f9a-e0acd6c668a1">GetLastPresentCount</a>
</td>
<td align="left" width="63%">
Returns the number of times the swapchain has been processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16eb0ec1-801a-4394-8d19-6d6d608be323">GetPresentStatistics</a>
</td>
<td align="left" width="63%">
Gets presentation statistics so an application can identify frames that do not have a Present method call.

</td>
</tr>
</table> 


## -remarks



There is always at least one swap chain for each device, known as the implicit swap chain. However, an additional swap chain for rendering multiple views from the same device can be created by calling the <a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">CreateAdditionalSwapChain</a> method.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The <b>LPDIRECT3DSWAPCHAIN9</b> and <b>PDIRECT3DSWAPCHAIN9</b> types are defined as pointers to the <a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a> interface.

<b>IDirect3DSwapChain9Ex</b> objects are returned as a pointer to an <a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a> object when <a href="https://msdn.microsoft.com/343522f2-33e8-46a5-a17f-b6c36b8fe82b">GetSwapChain</a> is called on an instance of <a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>.
The <b>IDirect3DSwapChain9Ex</b> interface is obtained by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the instance of <b>IDirect3DSwapChain9</b> that was returned by <b>GetSwapChain</b>.




## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">Feature Summary (Direct3D 9 for Windows Vista)</a>



<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

