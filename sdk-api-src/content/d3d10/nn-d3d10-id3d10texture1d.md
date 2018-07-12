---
UID: NN:d3d10.ID3D10Texture1D
title: ID3D10Texture1D
author: windows-sdk-content
description: A 1D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture1d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ID3D10Texture1D, ID3D10Texture1D interface [Direct3D 10], ID3D10Texture1D interface [Direct3D 10],described, d2aff301-d0e7-6d38-4b16-a1f90a64ba0e, d3d10/ID3D10Texture1D, direct3d10.id3d10texture1d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Texture1D
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture1D interface


## -description


A <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">1D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture1D</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>. <b>ID3D10Texture1D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Texture1D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173864(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173865(v=VS.85).aspx">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173866(v=VS.85).aspx">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource that was retrieved by <a href="https://msdn.microsoft.com/library/Bb173865(v=VS.85).aspx">ID3D10Texture1D::Map</a>, and re-enable the GPU's access to that resource.

</td>
</tr>
</table> 


## -remarks



To create an empty 1D texture, call <a href="https://msdn.microsoft.com/library/Bb173559(v=VS.85).aspx">ID3D10Device::CreateTexture1D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/library/Bb205131(v=VS.85).aspx">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/library/Bb205123(v=VS.85).aspx">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/library/Bb173556(v=VS.85).aspx">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/library/Bb173547(v=VS.85).aspx">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/library/Bb173558(v=VS.85).aspx">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/library/Bb205276(v=VS.85).aspx">Resource Interfaces</a>
 

 

