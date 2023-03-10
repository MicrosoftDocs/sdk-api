---
UID: NN:d3d12shader.ID3D12FunctionParameterReflection
title: ID3D12FunctionParameterReflection (d3d12shader.h)
description: A function-parameter-reflection interface accesses function-parameter info. (ID3D12FunctionParameterReflection)
helpviewer_keywords: ["ID3D12FunctionParameterReflection","ID3D12FunctionParameterReflection interface","ID3D12FunctionParameterReflection interface","described","d3d12shader/ID3D12FunctionParameterReflection","direct3d12.id3d12functionparameterreflection"]
old-location: direct3d12\id3d12functionparameterreflection.htm
tech.root: direct3d12
ms.assetid: 9AB312BE-E174-46D2-BF24-32309BD88AC4
ms.date: 12/05/2018
ms.keywords: ID3D12FunctionParameterReflection, ID3D12FunctionParameterReflection interface, ID3D12FunctionParameterReflection interface,described, d3d12shader/ID3D12FunctionParameterReflection, direct3d12.id3d12functionparameterreflection
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
 - ID3D12FunctionParameterReflection
 - d3d12shader/ID3D12FunctionParameterReflection
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
 - ID3D12FunctionParameterReflection
---

# ID3D12FunctionParameterReflection interface


## -description

A function-parameter-reflection interface accesses function-parameter info. 
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D12FunctionParameterReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12FunctionParameterReflection</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a function-parameter-reflection interface, call <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionreflection-getfunctionparameter">ID3D12FunctionReflection::GetFunctionParameter</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
      

<div class="alert"><b>Note</b>  <b>ID3D12FunctionParameterReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
