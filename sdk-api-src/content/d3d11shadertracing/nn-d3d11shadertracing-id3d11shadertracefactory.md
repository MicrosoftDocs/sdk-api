---
UID: NN:d3d11shadertracing.ID3D11ShaderTraceFactory
title: ID3D11ShaderTraceFactory
author: windows-sdk-content
description: An ID3D11ShaderTraceFactory interface implements a method for generating shader trace information objects.
old-location: direct3d11\id3d11shadertracefactory.htm
tech.root: direct3d11
ms.assetid: 0B90EA4B-0176-49DC-8A57-4D847552EFA3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ShaderTraceFactory, ID3D11ShaderTraceFactory interface [Direct3D 11], ID3D11ShaderTraceFactory interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTraceFactory, direct3d11.id3d11shadertracefactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D3D11SDKLayers.dll; D3D11_1SDKLayers.dll; D3D11_2SDKLayers.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11SDKLayers.dll
 - D3D11_1SDKLayers.dll
 - D3D11_2SDKLayers.dll
api_name:
 - ID3D11ShaderTraceFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderTraceFactory interface


## -description


An <b>ID3D11ShaderTraceFactory</b> interface implements a method for generating shader trace information objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderTraceFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11ShaderTraceFactory</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderTraceFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446844(v=VS.85).aspx">CreateShaderTrace</a>
</td>
<td align="left" width="63%">
Creates a shader-trace interface for a shader-trace information object.

</td>
</tr>
</table> 


## -remarks



These APIs require the Windows Software Development Kit (SDK) for Windows 8.

To retrieve an instance of <b>ID3D11ShaderTraceFactory</b>, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> on a <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> that you created with <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_DEBUGGABLE</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476161(v=VS.85).aspx">Shader Interfaces</a>
 

 

