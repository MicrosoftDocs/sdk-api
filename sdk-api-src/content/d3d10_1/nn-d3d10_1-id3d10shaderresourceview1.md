---
UID: NN:d3d10_1.ID3D10ShaderResourceView1
title: ID3D10ShaderResourceView1
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.
old-location: direct3d10\id3d10shaderresourceview1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderresourceview1.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
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


A shader-resource-view interface specifies the <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">subresources</a> a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderResourceView1</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>. <b>ID3D10ShaderResourceView1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/Bb694558(v=VS.85).aspx">GetDesc1</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/library/Bb694548(v=VS.85).aspx">ID3D10Device1::CreateShaderResourceView1</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/library/Bb173583(v=VS.85).aspx">ID3D10Device::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/library/Bb173629(v=VS.85).aspx">ID3D10Device::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/library/Bb173606(v=VS.85).aspx">ID3D10Device::PSSetShaderResources</a>.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>



<a href="https://msdn.microsoft.com/library/Bb205276(v=VS.85).aspx">Resource Interfaces</a>
 

 

