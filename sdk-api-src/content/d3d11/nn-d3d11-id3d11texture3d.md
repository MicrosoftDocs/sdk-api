---
UID: NN:d3d11.ID3D11Texture3D
title: ID3D11Texture3D
author: windows-sdk-content
description: A 3D texture interface accesses texel data, which is structured memory.
old-location: direct3d11\id3d11texture3d.htm
old-project: direct3d11
ms.assetid: 178d4ac4-c71f-40cb-bcaf-45ca96b36350
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 28ce947f-3bc9-9f8f-f8e7-667b8d30bf8e, ID3D11Texture3D, ID3D11Texture3D interface [Direct3D 11], ID3D11Texture3D interface [Direct3D 11],described, d3d11/ID3D11Texture3D, direct3d11.id3d11texture3d
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
 - ID3D11Texture3D
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Texture3D interface


## -description


A 3D texture interface accesses texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture3D</b> interface inherits from <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>. <b>ID3D11Texture3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Texture3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a2e2b93-148e-4070-9088-8ba5cbee6dcb">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture3D resource, call <a href="https://msdn.microsoft.com/92b31baf-2d64-47fe-bd0d-550f2a65ed9a">ID3D11Device::CreateTexture3D</a>. For info about how to create a 2D texture, which is similar to creating a 3D texture, see <a href="https://msdn.microsoft.com/dfe88635-b2c2-48f8-a21e-cce845b518fc">How to: Create a Texture</a>. 

Textures cannot be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">ID3D11Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

