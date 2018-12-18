---
UID: NN:d3d10_1shader.ID3D10ShaderReflection1
title: ID3D10ShaderReflection1
author: windows-sdk-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d10\id3d10shaderreflection1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10ShaderReflection1, ID3D10ShaderReflection1 interface [Direct3D 10], ID3D10ShaderReflection1 interface [Direct3D 10],described, c90dc2a0-8521-2e76-4417-146596886945, d3d10_1shader/ID3D10ShaderReflection1, direct3d10.id3d10shaderreflection1
ms.topic: interface
req.header: d3d10_1shader.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10ShaderReflection1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10ShaderReflection1 interface


## -description


A shader-reflection interface accesses shader information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflection1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173835(v=VS.85).aspx">ID3D10ShaderReflection</a>. <b>ID3D10ShaderReflection1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflection1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb694551(v=VS.85).aspx">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd607391(v=VS.85).aspx">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions used in a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb694552(v=VS.85).aspx">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb694553(v=VS.85).aspx">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb694554(v=VS.85).aspx">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd607392(v=VS.85).aspx">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Gets a resource binding description by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb694556(v=VS.85).aspx">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd607393(v=VS.85).aspx">IsLevel9Shader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd607394(v=VS.85).aspx">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.

</td>
</tr>
</table> 


## -remarks



This interface requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173835(v=VS.85).aspx">ID3D10ShaderReflection</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

