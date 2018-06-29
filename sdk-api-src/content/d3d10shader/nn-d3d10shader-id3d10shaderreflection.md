---
UID: NN:d3d10shader.ID3D10ShaderReflection
title: ID3D10ShaderReflection
author: windows-sdk-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d10\id3d10shaderreflection.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10ShaderReflection, ID3D10ShaderReflection interface [Direct3D 10], ID3D10ShaderReflection interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflection, direct3d10.id3d10shaderreflection, fd699fe1-b903-c976-14c4-3b0023611424
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
 - ID3D10ShaderReflection
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection interface


## -description


A shader-reflection interface accesses shader information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10ShaderReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173848(v=VS.85).aspx">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173849(v=VS.85).aspx">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173850(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173851(v=VS.85).aspx">GetInputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an input-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173852(v=VS.85).aspx">GetOutputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an output-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173853(v=VS.85).aspx">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Get a description of the resources bound to a shader.

</td>
</tr>
</table> 


## -remarks



Create the interface by calling <a href="https://msdn.microsoft.com/library/Bb310590(v=VS.85).aspx">D3DX10ReflectShader</a>. Since it is a COM interface, creating the interface increases a reference count and the interface must be released when it is no longer needed. The remaining shader-reflection interfaces are not COM interfaces.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

