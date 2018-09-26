---
UID: NN:d3d11.ID3D11DepthStencilState
title: ID3D11DepthStencilState
author: windows-sdk-content
description: The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the output-merger stage.
old-location: direct3d11\id3d11depthstencilstate.htm
tech.root: direct3d11
ms.assetid: cac22076-2ba6-4ab1-918e-8c9a7773acf6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11DepthStencilState, ID3D11DepthStencilState interface [Direct3D 11], ID3D11DepthStencilState interface [Direct3D 11],described, d3d11/ID3D11DepthStencilState, direct3d11.id3d11depthstencilstate, f7092d61-0b1d-daf2-0e96-635da5ebc121
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
 - ID3D11DepthStencilState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DepthStencilState interface


## -description


The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DepthStencilState</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11DepthStencilState</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11DepthStencilState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476376(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description for depth-stencil state that you used to create the depth-stencil-state object.

</td>
</tr>
</table> 


## -remarks



To create a depth-stencil-state object, call <a href="https://msdn.microsoft.com/en-us/library/Ff476506(v=VS.85).aspx">ID3D11Device::CreateDepthStencilState</a>. To bind the depth-stencil-state object to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>, call <a href="https://msdn.microsoft.com/en-us/library/Ff476463(v=VS.85).aspx">ID3D11DeviceContext::OMSetDepthStencilState</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

