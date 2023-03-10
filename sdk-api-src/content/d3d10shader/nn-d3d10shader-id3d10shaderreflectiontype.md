---
UID: NN:d3d10shader.ID3D10ShaderReflectionType
title: ID3D10ShaderReflectionType (d3d10shader.h)
description: This shader-reflection interface provides access to variable type. (ID3D10ShaderReflectionType)
helpviewer_keywords: ["07410292-1cdc-6e8c-f5a7-81000df37961","ID3D10ShaderReflectionType","ID3D10ShaderReflectionType interface [Direct3D 10]","ID3D10ShaderReflectionType interface [Direct3D 10]","described","d3d10shader/ID3D10ShaderReflectionType","direct3d10.id3d10shaderreflectiontype"]
old-location: direct3d10\id3d10shaderreflectiontype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectiontype.htm
ms.date: 12/05/2018
ms.keywords: 07410292-1cdc-6e8c-f5a7-81000df37961, ID3D10ShaderReflectionType, ID3D10ShaderReflectionType interface [Direct3D 10], ID3D10ShaderReflectionType interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionType, direct3d10.id3d10shaderreflectiontype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10ShaderReflectionType
 - d3d10shader/ID3D10ShaderReflectionType
dev_langs:
 - c++
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
---

# ID3D10ShaderReflectionType interface


## -description

This shader-reflection interface provides access to variable type.

## -inheritance

The <b>ID3D10ShaderReflectionType</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The get a shader-reflection-type interface, call <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionvariable-gettype">ID3D10ShaderReflectionVariable::GetType</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
