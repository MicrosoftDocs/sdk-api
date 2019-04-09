---
UID: NN:d3d10.ID3D10Texture2D
title: ID3D10Texture2D (d3d10.h)
author: windows-sdk-content
description: A 2D texture interface manages texel data, which is structured memory.
old-location: direct3d10\id3d10texture2d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9a2f06c7-c0b0-a077-da90-1fba199f3a88, ID3D10Texture2D, ID3D10Texture2D interface [Direct3D 10], ID3D10Texture2D interface [Direct3D 10],described, d3d10/ID3D10Texture2D, direct3d10.id3d10texture2d
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
 - ID3D10Texture2D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Texture2D interface


## -description


A <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a> interface manages texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture2D</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>. <b>ID3D10Texture2D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Texture2D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173868(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173869(v=VS.85).aspx">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173870(v=VS.85).aspx">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource that was retrieved by <a href="https://msdn.microsoft.com/en-us/library/Bb173869(v=VS.85).aspx">ID3D10Texture2D::Map</a>, and re-enable GPU access to the resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture2D resource, call <a href="https://msdn.microsoft.com/en-us/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/en-us/library/Bb205131(v=VS.85).aspx">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/en-us/library/Bb205123(v=VS.85).aspx">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/en-us/library/Bb173556(v=VS.85).aspx">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173547(v=VS.85).aspx">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173558(v=VS.85).aspx">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205276(v=VS.85).aspx">Resource Interfaces</a>
 

 

