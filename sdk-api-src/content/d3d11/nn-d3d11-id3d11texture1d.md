---
UID: NN:d3d11.ID3D11Texture1D
title: ID3D11Texture1D (d3d11.h)
author: windows-sdk-content
description: A 1D texture interface accesses texel data, which is structured memory.
old-location: direct3d11\id3d11texture1d.htm
tech.root: direct3d11
ms.assetid: 8f375031-014e-4eca-84d5-ebe40058f121
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 94d3cca2-802d-74ee-453b-b41e259e8903, ID3D11Texture1D, ID3D11Texture1D interface [Direct3D 11], ID3D11Texture1D interface [Direct3D 11],described, d3d11/ID3D11Texture1D, direct3d11.id3d11texture1d
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
 - ID3D11Texture1D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Texture1D interface


## -description


A 1D texture interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture1D</b> interface inherits from <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>. <b>ID3D11Texture1D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Texture1D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f806052d-ebdd-47c6-a92c-21d57831d2a9">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
</table> 


## -remarks



To create an empty 1D texture, call <a href="https://msdn.microsoft.com/34cdf984-8b2e-4ed3-a77b-b373752539f6">ID3D11Device::CreateTexture1D</a>. For info about how to create a 2D texture, which is similar to creating a 1D texture, see <a href="https://msdn.microsoft.com/dfe88635-b2c2-48f8-a21e-cce845b518fc">How to: Create a Texture</a>. 

Textures cannot be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">ID3D11Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

