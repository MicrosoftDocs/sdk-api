---
UID: NN:d3d10shader.ID3D10ShaderReflectionType
title: ID3D10ShaderReflectionType (d3d10shader.h)
description: This shader-reflection interface provides access to variable type.
helpviewer_keywords: ["07410292-1cdc-6e8c-f5a7-81000df37961","ID3D10ShaderReflectionType","ID3D10ShaderReflectionType interface [Direct3D 10]","ID3D10ShaderReflectionType interface [Direct3D 10]","described","d3d10shader/ID3D10ShaderReflectionType","direct3d10.id3d10shaderreflectiontype"]
old-location: direct3d10\id3d10shaderreflectiontype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectiontype.htm
ms.date: 12/05/2018
ms.keywords: 07410292-1cdc-6e8c-f5a7-81000df37961, ID3D10ShaderReflectionType, ID3D10ShaderReflectionType interface [Direct3D 10], ID3D10ShaderReflectionType interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionType, direct3d10.id3d10shaderreflectiontype
f1_keywords:
- d3d10shader/ID3D10ShaderReflectionType
dev_langs:
- c++
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
- ID3D10ShaderReflectionType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10ShaderReflectionType interface


## -description


This shader-reflection interface provides access to variable type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflectionType</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflectionType</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectiontype-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the description of a shader-reflection-variable type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectiontype-getmembertypebyindex">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectiontype-getmembertypebyname">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectiontype-getmembertypename">GetMemberTypeName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type.

</td>
</tr>
</table> 


## -remarks



The get a shader-reflection-type interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionvariable-gettype">ID3D10ShaderReflectionVariable::GetType</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
 

 

