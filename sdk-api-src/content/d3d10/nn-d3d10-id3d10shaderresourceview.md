---
UID: NN:d3d10.ID3D10ShaderResourceView
title: ID3D10ShaderResourceView (d3d10.h)
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.
old-location: direct3d10\id3d10shaderresourceview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderresourceview.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 52f9cfc5-67e6-4666-f34d-8344cdf131f0, ID3D10ShaderResourceView, ID3D10ShaderResourceView interface [Direct3D 10], ID3D10ShaderResourceView interface [Direct3D 10],described, d3d10/ID3D10ShaderResourceView, direct3d10.id3d10shaderresourceview
ms.topic: interface
f1_keywords: 
 - "d3d10/ID3D10ShaderResourceView"
req.header: d3d10.h
req.include-header: D3D10Shader.h
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
 - ID3D10ShaderResourceView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10ShaderResourceView interface


## -description


A shader-resource-view interface specifies the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresources</a> a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderResourceView</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>. <b>ID3D10ShaderResourceView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderResourceView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10shaderresourceview-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">ID3D10Device::GSSetShaderResources</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">ID3D10Device::VSSetShaderResources</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">ID3D10Device::PSSetShaderResources</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

