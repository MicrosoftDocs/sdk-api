---
UID: NN:d3d10shader.ID3D10ShaderReflectionType
title: ID3D10ShaderReflectionType
author: windows-sdk-content
description: This shader-reflection interface provides access to variable type.
old-location: direct3d10\id3d10shaderreflectiontype.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectiontype.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 07410292-1cdc-6e8c-f5a7-81000df37961, ID3D10ShaderReflectionType, ID3D10ShaderReflectionType interface [Direct3D 10], ID3D10ShaderReflectionType interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionType, direct3d10.id3d10shaderreflectiontype
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
 - ID3D10ShaderReflectionType
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10ShaderReflectionType interface


## -description


This shader-reflection interface provides access to variable type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflectionType</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflectionType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aafee47e-0b34-44af-9228-044be6eb1b53">GetDesc</a>
</td>
<td align="left" width="63%">
Get the description of a shader-reflection-variable type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/462fe507-41ad-4e7f-8a76-5f507e99167b">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62dc5221-77a1-4d2f-8c25-c18294ce25a0">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b3a49f6-b800-412f-90f3-a902ad59e798">GetMemberTypeName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type.

</td>
</tr>
</table> 


## -remarks



The get a shader-reflection-type interface, call <a href="https://msdn.microsoft.com/4a407589-122d-4d7c-944a-f63b0260a2fe">ID3D10ShaderReflectionVariable::GetType</a>.




## -see-also




<a href="https://msdn.microsoft.com/d8770b45-a05c-4dd8-9fa7-08fb4330d734">Shader Interfaces</a>
 

 

