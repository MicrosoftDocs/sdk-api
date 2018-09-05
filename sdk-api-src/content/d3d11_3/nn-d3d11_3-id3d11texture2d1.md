---
UID: NN:d3d11_3.ID3D11Texture2D1
title: ID3D11Texture2D1
author: windows-sdk-content
description: A 2D texture interface represents texel data, which is structured memory.
old-location: direct3d11\id3d11texture2d1.htm
old-project: direct3d11
ms.assetid: 0BEBF03C-CBE5-4988-AC98-76D90363A0B7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Texture2D1, ID3D11Texture2D1 interface [Direct3D 11], ID3D11Texture2D1 interface [Direct3D 11],described, d3d11_3/ID3D11Texture2D1, direct3d11.id3d11texture2d1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Texture2D1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11Texture2D1 interface


## -description


A 2D texture interface represents texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture2D1</b> interface inherits from <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>. <b>ID3D11Texture2D1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Texture2D1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/968FE780-90D8-44F8-AD31-BA29854413C4">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets the properties of the texture resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture2D resource, call <a href="https://msdn.microsoft.com/50C5789A-2C8E-49CB-9348-639CF8B971EC">ID3D11Device3::CreateTexture2D1</a>. For info about how to create a 2D texture, see <a href="https://msdn.microsoft.com/dfe88635-b2c2-48f8-a21e-cce845b518fc">How to: Create a Texture</a>. 

Textures can't be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render-target or depth-stencil resource, call <a href="https://msdn.microsoft.com/9B85B007-F8B0-43C1-999E-75E5243B7B5A">ID3D11Device3::CreateRenderTargetView1</a>, and <a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, call <a href="https://msdn.microsoft.com/50E072F2-EC3E-4BED-A230-5447ECD1E7D6">ID3D11Device3::CreateShaderResourceView1</a>.




## -see-also




<a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

