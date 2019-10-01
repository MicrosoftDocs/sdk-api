---
UID: NN:d3d11shader.ID3D11ShaderReflectionConstantBuffer
title: ID3D11ShaderReflectionConstantBuffer (d3d11shader.h)
author: windows-sdk-content
description: This shader-reflection interface provides access to a constant buffer.
old-location: direct3d11\id3d11shaderreflectionconstantbuffer.htm
tech.root: direct3d11
ms.assetid: 4b47ed8d-e814-4a7b-bc8e-25a8b71200ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 082bcb34-3d5a-3d3f-e3c1-0cf676c0b05b, ID3D11ShaderReflectionConstantBuffer, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11], ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionConstantBuffer, direct3d11.id3d11shaderreflectionconstantbuffer
ms.topic: interface
f1_keywords: 
 - "d3d11shader/ID3D11ShaderReflectionConstantBuffer"
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionConstantBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ShaderReflectionConstantBuffer interface


## -description


This shader-reflection interface provides access to a constant buffer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflectionConstantBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionConstantBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderReflectionConstantBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a constant-buffer description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getvariablebyindex">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Get a shader-reflection variable by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getvariablebyname">GetVariableByName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection variable by name.

</td>
</tr>
</table> 


## -remarks



To create a constant-buffer interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyindex">ID3D11ShaderReflection::GetConstantBufferByIndex</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyname">ID3D11ShaderReflection::GetConstantBufferByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

