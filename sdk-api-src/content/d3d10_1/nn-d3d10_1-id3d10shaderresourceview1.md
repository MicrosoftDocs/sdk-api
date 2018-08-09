---
UID: NN:d3d10_1.ID3D10ShaderResourceView1
title: ID3D10ShaderResourceView1
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.
old-location: direct3d10\id3d10shaderresourceview1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderresourceview1.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 42bd4307-40a4-6b0e-192f-643d483668e8, ID3D10ShaderResourceView1, ID3D10ShaderResourceView1 interface [Direct3D 10], ID3D10ShaderResourceView1 interface [Direct3D 10],described, d3d10_1/ID3D10ShaderResourceView1, direct3d10.id3d10shaderresourceview1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10_1.h
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
tech.root: 
req.typenames: D3D10_FEATURE_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10ShaderResourceView1
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderResourceView1 interface


## -description


A shader-resource-view interface specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a> a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderResourceView1</b> interface inherits from <a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView</a>. <b>ID3D10ShaderResourceView1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderResourceView1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b9b849a-1053-4554-9586-288386a7e853">GetDesc1</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/10a2ffe7-fb5b-4ba9-8b61-5a37b901b514">ID3D10Device1::CreateShaderResourceView1</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">ID3D10Device::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">ID3D10Device::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">ID3D10Device::PSSetShaderResources</a>.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

