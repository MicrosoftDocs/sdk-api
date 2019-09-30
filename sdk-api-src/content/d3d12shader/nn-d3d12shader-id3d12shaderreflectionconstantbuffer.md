---
UID: NN:d3d12shader.ID3D12ShaderReflectionConstantBuffer
title: ID3D12ShaderReflectionConstantBuffer (d3d12shader.h)
author: windows-sdk-content
description: This shader-reflection interface provides access to a constant buffer.
old-location: direct3d12\id3d12shaderreflectionconstantbuffer.htm
tech.root: direct3d12
ms.assetid: 4102AF77-3EC7-42CD-8B9C-6D0CC999529A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflectionConstantBuffer, ID3D12ShaderReflectionConstantBuffer interface, ID3D12ShaderReflectionConstantBuffer interface,described, d3d12shader/ID3D12ShaderReflectionConstantBuffer, direct3d12.id3d12shaderreflectionconstantbuffer
ms.topic: interface
f1_keywords: 
 - "d3d12shader/ID3D12ShaderReflectionConstantBuffer"
req.header: d3d12shader.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionConstantBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ShaderReflectionConstantBuffer interface


## -description


This shader-reflection interface provides access to a constant buffer.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionConstantBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflectionConstantBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ShaderReflectionConstantBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a constant-buffer description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getvariablebyindex">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection variable by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getvariablebyname">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection variable by name.
        

</td>
</tr>
</table> 


## -remarks



To create a constant-buffer interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyindex">ID3D12ShaderReflection::GetConstantBufferByIndex</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyname">ID3D12ShaderReflection::GetConstantBufferByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
 

 

