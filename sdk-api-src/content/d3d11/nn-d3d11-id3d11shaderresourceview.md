---
UID: NN:d3d11.ID3D11ShaderResourceView
title: ID3D11ShaderResourceView
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.
old-location: direct3d11\id3d11shaderresourceview.htm
old-project: direct3d11
ms.assetid: 289555d8-2a6e-454f-86bc-48fb2c8ea345
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 7665f23b-5b1b-14d0-93b2-1c24ed09a978, ID3D11ShaderResourceView, ID3D11ShaderResourceView interface [Direct3D 11], ID3D11ShaderResourceView interface [Direct3D 11],described, d3d11/ID3D11ShaderResourceView, direct3d11.id3d11shaderresourceview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ShaderResourceView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11ShaderResourceView interface


## -description


A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderResourceView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11ShaderResourceView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderResourceView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223bcf9c-a873-498c-af58-d93fe0a7f52c">GetDesc</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">ID3D11DeviceContext::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">ID3D11DeviceContext::PSSetShaderResources</a>.




## -see-also




<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

