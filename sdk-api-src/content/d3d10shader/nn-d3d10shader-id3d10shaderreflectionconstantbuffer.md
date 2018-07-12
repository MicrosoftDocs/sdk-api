---
UID: NN:d3d10shader.ID3D10ShaderReflectionConstantBuffer
title: ID3D10ShaderReflectionConstantBuffer
author: windows-sdk-content
description: This shader-reflection interface provides access to a constant buffer.
old-location: direct3d10\id3d10shaderreflectionconstantbuffer.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionconstantbuffer.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ID3D10ShaderReflectionConstantBuffer, ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10], ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionConstantBuffer, direct3d10.id3d10shaderreflectionconstantbuffer, fdeec4a2-cda3-d87b-9d10-c899b8675fd1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10shader.h
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
req.typenames: D3D10_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10ShaderReflectionConstantBuffer
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderReflectionConstantBuffer interface


## -description


This shader-reflection interface provides access to a constant buffer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflectionConstantBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10ShaderReflectionConstantBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflectionConstantBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173837(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a constant-buffer description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173838(v=VS.85).aspx">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Get a shader-reflection variable by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173839(v=VS.85).aspx">GetVariableByName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection variable by name.

</td>
</tr>
</table> 


## -remarks



To create a constant-buffer interface, call <a href="https://msdn.microsoft.com/library/Bb173848(v=VS.85).aspx">ID3D10ShaderReflection::GetConstantBufferByIndex</a> or <a href="https://msdn.microsoft.com/library/Bb173849(v=VS.85).aspx">ID3D10ShaderReflection::GetConstantBufferByName</a>. This is not a COM interface; therefore, you do not need to worry about reference counts or releasing the interface when you are done with it.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

