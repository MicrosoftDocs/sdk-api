---
UID: NN:d3d10.ID3D10Texture1D
title: ID3D10Texture1D
author: windows-driver-content
description: A 1D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture1d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D10Texture1D, ID3D10Texture1D interface [Direct3D 10], ID3D10Texture1D interface [Direct3D 10], described, d2aff301-d0e7-6d38-4b16-a1f90a64ba0e, d3d10/ID3D10Texture1D, direct3d10.id3d10texture1d
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Texture1D
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture1D interface


## -description


A <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">1D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture1D</b> interface inherits from <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>. <b>ID3D10Texture1D</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7a2b311d-c5ab-47d4-8d82-7a5980c57fa7">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67807061-166c-4d17-9677-f259c2676f75">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource that was retrieved by <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>, and re-enable the GPU's access to that resource.

</td>
</tr>
</table> 


## -remarks



To create an empty 1D texture, call <a href="https://msdn.microsoft.com/805e7bef-f4d5-4aa9-99a1-491e0518db7b">ID3D10Device::CreateTexture1D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/4c716be8-044e-4ed4-aeca-4379440826bd">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

