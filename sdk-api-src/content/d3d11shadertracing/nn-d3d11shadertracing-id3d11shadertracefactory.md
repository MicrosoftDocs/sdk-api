---
UID: NN:d3d11shadertracing.ID3D11ShaderTraceFactory
title: ID3D11ShaderTraceFactory
author: windows-sdk-content
description: An ID3D11ShaderTraceFactory interface implements a method for generating shader trace information objects.
old-location: direct3d11\id3d11shadertracefactory.htm
old-project: direct3d11
ms.assetid: 0B90EA4B-0176-49DC-8A57-4D847552EFA3
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11ShaderTraceFactory, ID3D11ShaderTraceFactory interface [Direct3D 11], ID3D11ShaderTraceFactory interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTraceFactory, direct3d11.id3d11shadertracefactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: D3D11_TRACE_REGISTER_TYPE
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
req.lib: 
req.dll: D3D11SDKLayers.dll; D3D11_1SDKLayers.dll; D3D11_2SDKLayers.dll
req.irql: 
---

# ID3D11ShaderTraceFactory interface


## -description


An <b>ID3D11ShaderTraceFactory</b> interface implements a method for generating shader trace information objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderTraceFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11ShaderTraceFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A">CreateShaderTrace</a>
</td>
<td align="left" width="63%">
Creates a shader-trace interface for a shader-trace information object.

</td>
</tr>
</table> 


## -remarks



These APIs require the Windows Software Development Kit (SDK) for Windows 8.

To retrieve an instance of <b>ID3D11ShaderTraceFactory</b>, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on a <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> that you created with <a href="d3d11_create_device_flag.htm">D3D11_CREATE_DEVICE_DEBUGGABLE</a>. 




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

