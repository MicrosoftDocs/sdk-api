---
UID: NN:d3d10.ID3D10Texture3D
title: ID3D10Texture3D (d3d10.h)
author: windows-sdk-content
description: A 3D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture3d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Texture3D, ID3D10Texture3D interface [Direct3D 10], ID3D10Texture3D interface [Direct3D 10],described, a0af960d-1977-383c-0ee3-09972ece4699, d3d10/ID3D10Texture3D, direct3d10.id3d10texture3d
ms.topic: interface
f1_keywords: 
 - "d3d10/ID3D10Texture3D"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Texture3D interface


## -description


A <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">3D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture3D</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>. <b>ID3D10Texture3D</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-map">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-unmap">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-map">ID3D10Texture3D::Map</a>, and re-enable the GPU's access to the resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture3D resource, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture3d">ID3D10Device::CreateTexture3D</a>. For more details on creating and loading textures, see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating-textures">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a>; instead, a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

