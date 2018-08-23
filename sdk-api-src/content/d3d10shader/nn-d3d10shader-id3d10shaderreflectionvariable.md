---
UID: NN:d3d10shader.ID3D10ShaderReflectionVariable
title: ID3D10ShaderReflectionVariable
author: windows-sdk-content
description: This shader-reflection interface provides access to a variable.
old-location: direct3d10\id3d10shaderreflectionvariable.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionvariable.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ID3D10ShaderReflectionVariable, ID3D10ShaderReflectionVariable interface [Direct3D 10], ID3D10ShaderReflectionVariable interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionVariable, direct3d10.id3d10shaderreflectionvariable, e8b67520-bfa7-7e41-f594-a51d5ad0301e
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10shader.h
req.include-header: 
req.redist: 
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
 - ID3D10ShaderReflectionVariable
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderReflectionVariable interface


## -description


This shader-reflection interface provides access to a variable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflectionVariable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflectionVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173846(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader-variable description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173847(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Get a shader-variable type.

</td>
</tr>
</table> 


## -remarks



To get a shader-reflection-variable interface, call a method like <a href="https://msdn.microsoft.com/en-us/library/Bb173838(v=VS.85).aspx">ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

