---
UID: NN:d3d11shader.ID3D11FunctionParameterReflection
title: ID3D11FunctionParameterReflection (d3d11shader.h)
description: A function-parameter-reflection interface accesses function-parameter info. (ID3D11FunctionParameterReflection)
helpviewer_keywords: ["ID3D11FunctionParameterReflection","ID3D11FunctionParameterReflection interface [Direct3D 11]","ID3D11FunctionParameterReflection interface [Direct3D 11]","described","d3d11shader/ID3D11FunctionParameterReflection","direct3d11.id3d11functionparameterreflection"]
old-location: direct3d11\id3d11functionparameterreflection.htm
tech.root: direct3d11
ms.assetid: EFF60EF7-C060-4148-916C-D971B65561F5
ms.date: 12/05/2018
ms.keywords: ID3D11FunctionParameterReflection, ID3D11FunctionParameterReflection interface [Direct3D 11], ID3D11FunctionParameterReflection interface [Direct3D 11],described, d3d11shader/ID3D11FunctionParameterReflection, direct3d11.id3d11functionparameterreflection
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11FunctionParameterReflection
 - d3d11shader/ID3D11FunctionParameterReflection
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
 - ID3D11FunctionParameterReflection
---

# ID3D11FunctionParameterReflection interface


## -description

A function-parameter-reflection interface accesses function-parameter info. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>

## -inheritance

The <b>ID3D11FunctionParameterReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11FunctionParameterReflection</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a function-parameter-reflection interface, call <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionreflection-getfunctionparameter">ID3D11FunctionReflection::GetFunctionParameter</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

<div class="alert"><b>Note</b>  <b>ID3D11FunctionParameterReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
