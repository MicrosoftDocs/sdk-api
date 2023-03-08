---
UID: NN:d3d12shader.ID3D12ShaderReflection
title: ID3D12ShaderReflection (d3d12shader.h)
description: A shader-reflection interface accesses shader information. (ID3D12ShaderReflection)
helpviewer_keywords: ["ID3D12ShaderReflection","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","described","d3d12shader/ID3D12ShaderReflection","direct3d12.id3d12shaderreflection"]
old-location: direct3d12\id3d12shaderreflection.htm
tech.root: direct3d12
ms.assetid: 145F2CCB-C076-42BE-8AF4-74349CDF6B02
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflection, ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,described, d3d12shader/ID3D12ShaderReflection, direct3d12.id3d12shaderreflection
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
 - ID3D12ShaderReflection
 - d3d12shader/ID3D12ShaderReflection
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
 - ID3D12ShaderReflection
---

## -description

A shader-reflection interface accesses shader information.

## -inheritance

The <b>ID3D12ShaderReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflection</b> also has these types of members:

## -remarks

An <b>ID3D12ShaderReflection</b> interface can be retrieved for a shader by using <a href="/windows/desktop/direct3dhlsl/d3dreflect">D3DReflect</a>.

> [!NOTE]
> This function from `d3dcompiler.dll` supports Shader Model 2 - 5.1. For Shader Model 6 shader reflection, see `dxcompiler.dll` and  [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
