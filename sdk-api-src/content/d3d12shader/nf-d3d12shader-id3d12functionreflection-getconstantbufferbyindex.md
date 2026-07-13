---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetConstantBufferByIndex
title: ID3D12FunctionReflection::GetConstantBufferByIndex (d3d12shader.h)
description: The ID3D12FunctionReflection::GetConstantBufferByIndex method (d3d12shader.h) gets a constant buffer by index for a function.
helpviewer_keywords: ["GetConstantBufferByIndex","GetConstantBufferByIndex method","GetConstantBufferByIndex method","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","GetConstantBufferByIndex method","ID3D12FunctionReflection.GetConstantBufferByIndex","ID3D12FunctionReflection::GetConstantBufferByIndex","d3d12shader/ID3D12FunctionReflection::GetConstantBufferByIndex","direct3d12.id3d12functionreflection_getconstantbufferbyindex"]
old-location: direct3d12\id3d12functionreflection_getconstantbufferbyindex.htm
tech.root: direct3d12
ms.assetid: 4B953072-DEF0-4A30-93A1-247B0C2CAFA3
ms.date: 08/10/2022
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method, GetConstantBufferByIndex method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetConstantBufferByIndex method, ID3D12FunctionReflection.GetConstantBufferByIndex, ID3D12FunctionReflection::GetConstantBufferByIndex, d3d12shader/ID3D12FunctionReflection::GetConstantBufferByIndex, direct3d12.id3d12functionreflection_getconstantbufferbyindex
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
 - ID3D12FunctionReflection::GetConstantBufferByIndex
 - d3d12shader/ID3D12FunctionReflection::GetConstantBufferByIndex
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
 - ID3D12FunctionReflection.GetConstantBufferByIndex
---

# ID3D12FunctionReflection::GetConstantBufferByIndex


## -description

Gets a constant buffer by index for a function.

## -parameters

### -param BufferIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader.
        A shader can use one or more constant buffers.
        For best performance, separate constants into buffers based on the frequency they are updated.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>