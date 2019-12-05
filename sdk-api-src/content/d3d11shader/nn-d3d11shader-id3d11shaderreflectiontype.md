---
UID: NN:d3d11shader.ID3D11ShaderReflectionType
title: ID3D11ShaderReflectionType (d3d11shader.h)
description: This shader-reflection interface provides access to variable type.
old-location: direct3d11\id3d11shaderreflectiontype.htm
tech.root: direct3d11
ms.assetid: 04520be2-2491-4f10-988a-e203659efddf
ms.date: 12/05/2018
ms.keywords: 369c707d-0441-c514-603f-48f54b69b778, ID3D11ShaderReflectionType, ID3D11ShaderReflectionType interface [Direct3D 11], ID3D11ShaderReflectionType interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionType, direct3d11.id3d11shaderreflectiontype
ms.topic: interface
f1_keywords:
- d3d11shader/ID3D11ShaderReflectionType
dev_langs:
- c++
req.header: d3d11shader.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCompiler_47.dll
api_name:
- ID3D11ShaderReflectionType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ShaderReflectionType interface


## -description


This shader-reflection interface provides access to variable type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflectionType</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderReflectionType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getbaseclass">GetBaseClass</a>
</td>
<td align="left" width="63%">
Gets an <b>ID3D11ShaderReflectionType Interface</b>  interface containing the variable base class type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the description of a shader-reflection-variable type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getinterfacebyindex">GetInterfaceByIndex</a>
</td>
<td align="left" width="63%">
Get an interface by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getmembertypebyindex">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getmembertypebyname">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getmembertypename">GetMemberTypeName</a>
</td>
<td align="left" width="63%">
Get a shader-reflection-variable type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getnuminterfaces">GetNumInterfaces</a>
</td>
<td align="left" width="63%">
Gets the number of interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-getsubtype">GetSubType</a>
</td>
<td align="left" width="63%">
Gets the base class of a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-implementsinterface">ImplementsInterface</a>
</td>
<td align="left" width="63%">
Indicates whether a class type implements an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Indicates whether two <b>ID3D11ShaderReflectionType Interface</b> pointers have the same underlying type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectiontype-isoftype">IsOfType</a>
</td>
<td align="left" width="63%">
Indicates whether a variable is of the specified type.

</td>
</tr>
</table> 


## -remarks



The get a shader-reflection-type interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-gettype">ID3D11ShaderReflectionVariable::GetType</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

