---
UID: NN:d3d12shader.ID3D12ShaderReflectionType
title: ID3D12ShaderReflectionType (d3d12shader.h)
description: This shader-reflection interface provides access to variable type. (ID3D12ShaderReflectionType)
helpviewer_keywords: ["ID3D12ShaderReflectionType","ID3D12ShaderReflectionType interface","ID3D12ShaderReflectionType interface","described","d3d12shader/ID3D12ShaderReflectionType","direct3d12.id3d12shaderreflectiontype"]
old-location: direct3d12\id3d12shaderreflectiontype.htm
tech.root: direct3d12
ms.assetid: 78FF30C5-7F23-489D-9E9D-916F6CE09C0E
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflectionType, ID3D12ShaderReflectionType interface, ID3D12ShaderReflectionType interface,described, d3d12shader/ID3D12ShaderReflectionType, direct3d12.id3d12shaderreflectiontype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12ShaderReflectionType
 - d3d12shader/ID3D12ShaderReflectionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionType
---

# ID3D12ShaderReflectionType interface


## -description

This shader-reflection interface provides access to variable type.

## -inheritance

The <b>ID3D12ShaderReflectionType</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The get a shader-reflection-type interface, call <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionvariable-gettype">ID3D12ShaderReflectionVariable::GetType</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
