---
UID: NN:d3d11.ID3D11ShaderResourceView
title: ID3D11ShaderResourceView
author: windows-sdk-content
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.
old-location: direct3d11\id3d11shaderresourceview.htm
tech.root: direct3d11
ms.assetid: 289555d8-2a6e-454f-86bc-48fb2c8ea345
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 7665f23b-5b1b-14d0-93b2-1c24ed09a978, ID3D11ShaderResourceView, ID3D11ShaderResourceView interface [Direct3D 11], ID3D11ShaderResourceView interface [Direct3D 11],described, d3d11/ID3D11ShaderResourceView, direct3d11.id3d11shaderresourceview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11ShaderResourceView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderResourceView interface


## -description


A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderResourceView</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>. <b>ID3D11ShaderResourceView</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476629(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the shader resource view's description.

</td>
</tr>
</table> 


## -remarks



To create a shader-resource view, call <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="https://msdn.microsoft.com/en-us/library/Ff476439(v=VS.85).aspx">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/en-us/library/Ff476494(v=VS.85).aspx">ID3D11DeviceContext::VSSetShaderResources</a> or <a href="https://msdn.microsoft.com/en-us/library/Ff476473(v=VS.85).aspx">ID3D11DeviceContext::PSSetShaderResources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476172(v=VS.85).aspx">Resource Interfaces</a>
 

 

