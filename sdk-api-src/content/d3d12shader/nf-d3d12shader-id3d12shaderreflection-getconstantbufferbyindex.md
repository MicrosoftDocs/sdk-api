---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetConstantBufferByIndex
title: ID3D12ShaderReflection::GetConstantBufferByIndex (d3d12shader.h)
description: Gets a constant buffer by index.
helpviewer_keywords: ["GetConstantBufferByIndex","GetConstantBufferByIndex method","GetConstantBufferByIndex method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetConstantBufferByIndex method","ID3D12ShaderReflection.GetConstantBufferByIndex","ID3D12ShaderReflection::GetConstantBufferByIndex","d3d12shader/ID3D12ShaderReflection::GetConstantBufferByIndex","direct3d12.id3d12shaderreflection_getconstantbufferbyindex"]
old-location: direct3d12\id3d12shaderreflection_getconstantbufferbyindex.htm
tech.root: direct3d12
ms.assetid: 84E3240C-D21F-4F71-9AC2-C89570571A72
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method, GetConstantBufferByIndex method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetConstantBufferByIndex method, ID3D12ShaderReflection.GetConstantBufferByIndex, ID3D12ShaderReflection::GetConstantBufferByIndex, d3d12shader/ID3D12ShaderReflection::GetConstantBufferByIndex, direct3d12.id3d12shaderreflection_getconstantbufferbyindex
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
 - ID3D12ShaderReflection::GetConstantBufferByIndex
 - d3d12shader/ID3D12ShaderReflection::GetConstantBufferByIndex
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
 - ID3D12ShaderReflection.GetConstantBufferByIndex
---

# ID3D12ShaderReflection::GetConstantBufferByIndex


## -description

Gets a constant buffer by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer Interface</a>).

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>