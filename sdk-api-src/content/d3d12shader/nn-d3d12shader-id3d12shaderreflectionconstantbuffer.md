---
UID: NN:d3d12shader.ID3D12ShaderReflectionConstantBuffer
title: ID3D12ShaderReflectionConstantBuffer
author: windows-sdk-content
description: This shader-reflection interface provides access to a constant buffer.
old-location: direct3d12\id3d12shaderreflectionconstantbuffer.htm
old-project: direct3d12
ms.assetid: 4102AF77-3EC7-42CD-8B9C-6D0CC999529A
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12ShaderReflectionConstantBuffer, ID3D12ShaderReflectionConstantBuffer interface, ID3D12ShaderReflectionConstantBuffer interface,described, d3d12shader/ID3D12ShaderReflectionConstantBuffer, direct3d12.id3d12shaderreflectionconstantbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionConstantBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionConstantBuffer interface


## -description


This shader-reflection interface provides access to a constant buffer.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionConstantBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12ShaderReflectionConstantBuffer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/33D6926F-BF1B-4424-BC28-83F8A4A30589">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a constant-buffer description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F7083A4D-ADD4-4C6F-A031-ABF16A3C351C">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection variable by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD18A64F-9B4A-42FE-8E18-13E9375E19BC">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection variable by name.
        

</td>
</tr>
</table> 


## -remarks



To create a constant-buffer interface, call <a href="https://msdn.microsoft.com/84E3240C-D21F-4F71-9AC2-C89570571A72">ID3D12ShaderReflection::GetConstantBufferByIndex</a> or <a href="https://msdn.microsoft.com/C8BE8C17-2B5A-45AB-8C39-778FFFA78992">ID3D12ShaderReflection::GetConstantBufferByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

