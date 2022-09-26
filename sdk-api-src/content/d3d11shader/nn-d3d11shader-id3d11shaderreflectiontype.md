---
UID: NN:d3d11shader.ID3D11ShaderReflectionType
title: ID3D11ShaderReflectionType (d3d11shader.h)
description: This shader-reflection interface provides access to variable type. (ID3D11ShaderReflectionType)
helpviewer_keywords: ["369c707d-0441-c514-603f-48f54b69b778","ID3D11ShaderReflectionType","ID3D11ShaderReflectionType interface [Direct3D 11]","ID3D11ShaderReflectionType interface [Direct3D 11]","described","d3d11shader/ID3D11ShaderReflectionType","direct3d11.id3d11shaderreflectiontype"]
old-location: direct3d11\id3d11shaderreflectiontype.htm
tech.root: direct3d11
ms.assetid: 04520be2-2491-4f10-988a-e203659efddf
ms.date: 12/05/2018
ms.keywords: 369c707d-0441-c514-603f-48f54b69b778, ID3D11ShaderReflectionType, ID3D11ShaderReflectionType interface [Direct3D 11], ID3D11ShaderReflectionType interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionType, direct3d11.id3d11shaderreflectiontype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflectionType
 - d3d11shader/ID3D11ShaderReflectionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionType
---

# ID3D11ShaderReflectionType interface


## -description

This shader-reflection interface provides access to variable type.

## -inheritance

The <b>ID3D11ShaderReflectionType</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The get a shader-reflection-type interface, call <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-gettype">ID3D11ShaderReflectionVariable::GetType</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
