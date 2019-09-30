---
UID: NN:d3d12shader.ID3D12ShaderReflectionType
title: ID3D12ShaderReflectionType (d3d12shader.h)
author: windows-sdk-content
description: This shader-reflection interface provides access to variable type.
old-location: direct3d12\id3d12shaderreflectiontype.htm
tech.root: direct3d12
ms.assetid: 78FF30C5-7F23-489D-9E9D-916F6CE09C0E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflectionType, ID3D12ShaderReflectionType interface, ID3D12ShaderReflectionType interface,described, d3d12shader/ID3D12ShaderReflectionType, direct3d12.id3d12shaderreflectiontype
ms.topic: interface
f1_keywords: 
 - "d3d12shader/ID3D12ShaderReflectionType"
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
 - ID3D12ShaderReflectionType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ShaderReflectionType interface


## -description


This shader-reflection interface provides access to variable type.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionType</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ShaderReflectionType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getbaseclass">GetBaseClass</a>
</td>
<td align="left" width="63%">
Gets an <b>ID3D12ShaderReflectionType Interface</b>  interface containing the variable base class type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description of a shader-reflection-variable type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getinterfacebyindex">GetInterfaceByIndex</a>
</td>
<td align="left" width="63%">
Gets an interface by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getmembertypebyindex">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getmembertypebyname">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getmembertypename">GetMemberTypeName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getnuminterfaces">GetNumInterfaces</a>
</td>
<td align="left" width="63%">
Gets the number of interfaces.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-getsubtype">GetSubType</a>
</td>
<td align="left" width="63%">
Gets the base class of a class.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-implementsinterface">ImplementsInterface</a>
</td>
<td align="left" width="63%">
Indicates whether a class type implements an interface.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Indicates whether two <b>ID3D12ShaderReflectionType Interface</b> pointers have the same underlying type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectiontype-isoftype">IsOfType</a>
</td>
<td align="left" width="63%">
Indicates whether a variable is of the specified type.
        

</td>
</tr>
</table> 


## -remarks



The get a shader-reflection-type interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionvariable-gettype">ID3D12ShaderReflectionVariable::GetType</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
 

 

