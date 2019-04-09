---
UID: NN:d3d11_3.ID3D11ShaderResourceView1
title: ID3D11ShaderResourceView1 (d3d11_3.h)
author: windows-sdk-content
description: A shader-resource-view interface represents the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.
old-location: direct3d11\id3d11shaderresourceview1.htm
tech.root: direct3d11
ms.assetid: 5AF5DCAC-2C3A-45A7-A165-3FBE3E0D5CAB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderResourceView1, ID3D11ShaderResourceView1 interface [Direct3D 11], ID3D11ShaderResourceView1 interface [Direct3D 11],described, d3d11_3/ID3D11ShaderResourceView1, direct3d11.id3d11shaderresourceview1
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ShaderResourceView1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderResourceView1 interface


## -description


A shader-resource-view interface represents the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderResourceView1</b> interface inherits from <a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>. <b>ID3D11ShaderResourceView1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderResourceView1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0551927-0BDA-4C26-9F35-0A96B83A2617">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets the shader-resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/50E072F2-EC3E-4BED-A230-5447ECD1E7D6">ID3D11Device3::CreateShaderResourceView1</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">ID3D11DeviceContext::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">ID3D11DeviceContext::PSSetShaderResources</a>.




## -see-also




<a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

