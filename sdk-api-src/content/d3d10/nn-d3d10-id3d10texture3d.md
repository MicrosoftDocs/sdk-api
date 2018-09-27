---
UID: NN:d3d10.ID3D10Texture3D
title: ID3D10Texture3D
author: windows-sdk-content
description: A 3D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture3d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D10Texture3D, ID3D10Texture3D interface [Direct3D 10], ID3D10Texture3D interface [Direct3D 10],described, a0af960d-1977-383c-0ee3-09972ece4699, d3d10/ID3D10Texture3D, direct3d10.id3d10texture3d
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Texture3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Texture3D interface


## -description


A <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">3D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture3D</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>. <b>ID3D10Texture3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Texture3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173872(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173873(v=VS.85).aspx">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173874(v=VS.85).aspx">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource retrieved by <a href="https://msdn.microsoft.com/en-us/library/Bb173873(v=VS.85).aspx">ID3D10Texture3D::Map</a>, and re-enable the GPU's access to the resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture3D resource, call <a href="https://msdn.microsoft.com/en-us/library/Bb173561(v=VS.85).aspx">ID3D10Device::CreateTexture3D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/en-us/library/Bb205131(v=VS.85).aspx">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/en-us/library/Bb205123(v=VS.85).aspx">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/en-us/library/Bb173556(v=VS.85).aspx">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173547(v=VS.85).aspx">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173558(v=VS.85).aspx">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205276(v=VS.85).aspx">Resource Interfaces</a>
 

 

