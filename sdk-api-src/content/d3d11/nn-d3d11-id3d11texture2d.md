---
UID: NN:d3d11.ID3D11Texture2D
title: ID3D11Texture2D
author: windows-sdk-content
description: A 2D texture interface manages texel data, which is structured memory.
old-location: direct3d11\id3d11texture2d.htm
tech.root: direct3d11
ms.assetid: 49cd6e21-6cb1-45ea-b83a-3c93f0560915
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 92f1d183-b220-944f-113a-e7696cd05d2f, ID3D11Texture2D, ID3D11Texture2D interface [Direct3D 11], ID3D11Texture2D interface [Direct3D 11],described, d3d11/ID3D11Texture2D, direct3d11.id3d11texture2d
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
 - ID3D11Texture2D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Texture2D interface


## -description


A 2D texture interface manages texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture2D</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>. <b>ID3D11Texture2D</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Texture2D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476636(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of the texture resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture2D resource, call <a href="https://msdn.microsoft.com/en-us/library/Ff476521(v=VS.85).aspx">ID3D11Device::CreateTexture2D</a>. For info about how to create a 2D texture, see <a href="https://msdn.microsoft.com/en-us/library/Ff476903(v=VS.85).aspx">How to: Create a Texture</a>. 

Textures cannot be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="https://msdn.microsoft.com/en-us/library/Ff476517(v=VS.85).aspx">ID3D11Device::CreateRenderTargetView</a>, and <a href="https://msdn.microsoft.com/en-us/library/Ff476507(v=VS.85).aspx">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476172(v=VS.85).aspx">Resource Interfaces</a>
 

 

