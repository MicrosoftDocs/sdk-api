---
UID: NN:d3d10.ID3D10Texture2D
title: ID3D10Texture2D
author: windows-driver-content
description: A 2D texture interface manages texel data, which is structured memory.
old-location: direct3d10\id3d10texture2d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 9a2f06c7-c0b0-a077-da90-1fba199f3a88, ID3D10Texture2D, ID3D10Texture2D interface [Direct3D 10], ID3D10Texture2D interface [Direct3D 10],described, d3d10/ID3D10Texture2D, direct3d10.id3d10texture2d
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
-	ID3D10Texture2D
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture2D interface


## -description


A <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D texture</a> interface manages texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture2D</b> interface inherits from <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>. <b>ID3D10Texture2D</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/304ba616-457d-49c2-aa91-6f8e45755345">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac00017a-2659-43ac-bba1-d8d8febb3cd4">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource that was retrieved by <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">ID3D10Texture2D::Map</a>, and re-enable GPU access to the resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture2D resource, call <a href="https://msdn.microsoft.com/1f9e81e1-721c-4895-9196-2be3e5b260fd">ID3D10Device::CreateTexture2D</a>. For more details on creating and loading textures, see <a href="https://msdn.microsoft.com/4c716be8-044e-4ed4-aeca-4379440826bd">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">pipeline</a>; instead, a <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

