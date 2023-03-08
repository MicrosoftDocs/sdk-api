---
UID: NN:d3d11shader.ID3D11ShaderReflectionVariable
title: ID3D11ShaderReflectionVariable (d3d11shader.h)
description: This shader-reflection interface provides access to a variable. (ID3D11ShaderReflectionVariable)
helpviewer_keywords: ["ID3D11ShaderReflectionVariable","ID3D11ShaderReflectionVariable interface [Direct3D 11]","ID3D11ShaderReflectionVariable interface [Direct3D 11]","described","d3d11shader/ID3D11ShaderReflectionVariable","direct3d11.id3d11shaderreflectionvariable","f2ebf92b-2932-5cc0-239f-7e9b48dec05f"]
old-location: direct3d11\id3d11shaderreflectionvariable.htm
tech.root: direct3d11
ms.assetid: 4422a51f-b190-4df0-a1bb-a8ee2cc66da2
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderReflectionVariable, ID3D11ShaderReflectionVariable interface [Direct3D 11], ID3D11ShaderReflectionVariable interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionVariable, direct3d11.id3d11shaderreflectionvariable, f2ebf92b-2932-5cc0-239f-7e9b48dec05f
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
 - ID3D11ShaderReflectionVariable
 - d3d11shader/ID3D11ShaderReflectionVariable
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
 - ID3D11ShaderReflectionVariable
---

# ID3D11ShaderReflectionVariable interface


## -description

This shader-reflection interface provides access to a variable.

## -inheritance

The <b>ID3D11ShaderReflectionVariable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a shader-reflection-variable interface, call a method like <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname">ID3D11ShaderReflection::GetVariableByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
