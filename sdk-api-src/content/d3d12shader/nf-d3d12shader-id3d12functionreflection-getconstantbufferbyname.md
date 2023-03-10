---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetConstantBufferByName
title: ID3D12FunctionReflection::GetConstantBufferByName (d3d12shader.h)
description: Gets a constant buffer by name for a function. (ID3D12FunctionReflection.GetConstantBufferByName)
helpviewer_keywords: ["GetConstantBufferByName","GetConstantBufferByName method","GetConstantBufferByName method","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","GetConstantBufferByName method","ID3D12FunctionReflection.GetConstantBufferByName","ID3D12FunctionReflection::GetConstantBufferByName","d3d12shader/ID3D12FunctionReflection::GetConstantBufferByName","direct3d12.id3d12functionreflection_getconstantbufferbyname"]
old-location: direct3d12\id3d12functionreflection_getconstantbufferbyname.htm
tech.root: direct3d12
ms.assetid: AB781E44-2FCE-4E20-955C-C6F9F6F3064B
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method, GetConstantBufferByName method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetConstantBufferByName method, ID3D12FunctionReflection.GetConstantBufferByName, ID3D12FunctionReflection::GetConstantBufferByName, d3d12shader/ID3D12FunctionReflection::GetConstantBufferByName, direct3d12.id3d12functionreflection_getconstantbufferbyname
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
 - ID3D12FunctionReflection::GetConstantBufferByName
 - d3d12shader/ID3D12FunctionReflection::GetConstantBufferByName
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
 - ID3D12FunctionReflection.GetConstantBufferByName
---

# ID3D12FunctionReflection::GetConstantBufferByName


## -description

Gets a constant buffer by name for a function.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>
