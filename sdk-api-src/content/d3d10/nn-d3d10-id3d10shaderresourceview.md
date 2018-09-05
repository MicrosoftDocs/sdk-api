---
UID: NN:d3d10.ID3D10ShaderResourceView
title: ID3D10ShaderResourceView
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.
old-location: direct3d10\id3d10shaderresourceview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderresourceview.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 52f9cfc5-67e6-4666-f34d-8344cdf131f0, ID3D10ShaderResourceView, ID3D10ShaderResourceView interface [Direct3D 10], ID3D10ShaderResourceView interface [Direct3D 10],described, d3d10/ID3D10ShaderResourceView, direct3d10.id3d10shaderresourceview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
req.include-header: D3D10Shader.h
req.redist: 
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
 - ID3D10ShaderResourceView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderResourceView interface


## -description


A shader-resource-view interface specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a> a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderResourceView</b> interface inherits from <a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>. <b>ID3D10ShaderResourceView</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/29550424-d1a3-4ce4-87b0-bd2be4f465fe">GetDesc</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">ID3D10Device::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">ID3D10Device::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">ID3D10Device::PSSetShaderResources</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

