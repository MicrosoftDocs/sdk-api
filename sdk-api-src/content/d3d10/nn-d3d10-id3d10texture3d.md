---
UID: NN:d3d10.ID3D10Texture3D
title: ID3D10Texture3D
author: windows-sdk-content
description: A 3D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture3d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
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
 - ID3D10Texture3D
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture3D interface


## -description


A <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">3D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture3D</b> interface inherits from <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>. <b>ID3D10Texture3D</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2360cb66-aace-4ab7-ad46-e62f0be11f1d">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/109e2d24-9e57-4db1-9d0f-8cdd06828436">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource retrieved by <a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">ID3D10Texture3D::Map</a>, and re-enable the GPU's access to the resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture3D resource, call <a href="https://msdn.microsoft.com/4f57a2e5-c663-46c3-a092-798a15cf9154">ID3D10Device::CreateTexture3D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/4c716be8-044e-4ed4-aeca-4379440826bd">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

