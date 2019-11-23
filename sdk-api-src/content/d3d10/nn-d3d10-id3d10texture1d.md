---
UID: NN:d3d10.ID3D10Texture1D
title: ID3D10Texture1D (d3d10.h)

description: A 1D texture interface accesses texel data, which is structured memory.
old-location: direct3d10\id3d10texture1d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d.htm

ms.date: 12/05/2018
ms.keywords: ID3D10Texture1D, ID3D10Texture1D interface [Direct3D 10], ID3D10Texture1D interface [Direct3D 10],described, d2aff301-d0e7-6d38-4b16-a1f90a64ba0e, d3d10/ID3D10Texture1D, direct3d10.id3d10texture1d
ms.topic: interface
f1_keywords: 
 - "d3d10/ID3D10Texture1D"
dev_langs:
 - c++
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
 - ID3D10Texture1D
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Texture1D interface


## -description


A <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a> interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Texture1D</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>. <b>ID3D10Texture1D</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-map">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-unmap">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource that was retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-map">ID3D10Texture1D::Map</a>, and re-enable the GPU's access to that resource.

</td>
</tr>
</table> 


## -remarks



To create an empty 1D texture, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture1d">ID3D10Device::CreateTexture1D</a>. For more details on creating and loading textures, see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating-textures">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a>; instead, a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

