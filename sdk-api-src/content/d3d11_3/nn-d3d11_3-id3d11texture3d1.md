---
UID: NN:d3d11_3.ID3D11Texture3D1
title: ID3D11Texture3D1
author: windows-sdk-content
description: A 3D texture interface represents texel data, which is structured memory.
old-location: direct3d11\id3d11texture3d1.htm
tech.root: direct3d11
ms.assetid: 8ADF6845-BC62-4FCC-946E-7DE676C250B0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11Texture3D1, ID3D11Texture3D1 interface [Direct3D 11], ID3D11Texture3D1 interface [Direct3D 11],described, d3d11_3/ID3D11Texture3D1, direct3d11.id3d11texture3d1
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D11Texture3D1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Texture3D1 interface


## -description


A 3D texture interface represents texel data, which is structured memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture3D1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476637(v=VS.85).aspx">ID3D11Texture3D</a>. <b>ID3D11Texture3D1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Texture3D1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899247(v=VS.85).aspx">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets the properties of the texture resource.

</td>
</tr>
</table> 


## -remarks



To create an empty Texture3D resource, call <a href="https://msdn.microsoft.com/en-us/library/Dn899231(v=VS.85).aspx">ID3D11Device3::CreateTexture3D1</a>. For info about how to create a 2D texture, which is similar to creating a 3D texture, see <a href="https://msdn.microsoft.com/en-us/library/Ff476903(v=VS.85).aspx">How to: Create a Texture</a>. 

Textures can't be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render-target or depth-stencil resource, call <a href="https://msdn.microsoft.com/en-us/library/Dn899224(v=VS.85).aspx">ID3D11Device3::CreateRenderTargetView1</a>, and <a href="https://msdn.microsoft.com/en-us/library/Ff476507(v=VS.85).aspx">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, call <a href="https://msdn.microsoft.com/en-us/library/Dn899227(v=VS.85).aspx">ID3D11Device3::CreateShaderResourceView1</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476637(v=VS.85).aspx">ID3D11Texture3D</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476172(v=VS.85).aspx">Resource Interfaces</a>
 

 

