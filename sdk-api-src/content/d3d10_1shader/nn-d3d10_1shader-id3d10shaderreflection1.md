---
UID: NN:d3d10_1shader.ID3D10ShaderReflection1
title: ID3D10ShaderReflection1
author: windows-driver-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d10\id3d10shaderreflection1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ID3D10ShaderReflection1, ID3D10ShaderReflection1 interface [Direct3D 10], ID3D10ShaderReflection1 interface [Direct3D 10],described, c90dc2a0-8521-2e76-4417-146596886945, d3d10_1shader/ID3D10ShaderReflection1, direct3d10.id3d10shaderreflection1
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D10_SHADER_DEBUG_VARTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10ShaderReflection1
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection1 interface


## -description


A shader-reflection interface accesses shader information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflection1</b> interface inherits from <a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection</a>. <b>ID3D10ShaderReflection1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fd7a9c67-3b73-4f6d-b553-cf906f7dfd38">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b1639c2-12d6-47ed-8142-93c4a5e9ca41">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions used in a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba25ade-e3a3-40fe-8555-2fcb07dc0ed3">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1984390c-c4fe-4c04-bd4b-c1a815454bc2">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b791bb7-dc94-493b-98c8-d18139f984d2">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3171c33f-36dd-4e19-8472-294f62b2d90d">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Gets a resource binding description by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60cedf83-f3f8-48d5-8e45-aafb09b686bd">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f264e3ae-737f-4e9a-a743-08d2d697eb61">IsLevel9Shader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92e0e0a2-1b9c-4324-8cda-22beef322583">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.

</td>
</tr>
</table> 


## -remarks



This interface requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection</a>



<a href="https://msdn.microsoft.com/d8770b45-a05c-4dd8-9fa7-08fb4330d734">Shader Interfaces</a>
 

 

