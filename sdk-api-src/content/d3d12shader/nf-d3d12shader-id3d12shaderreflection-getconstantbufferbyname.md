---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetConstantBufferByName
title: ID3D12ShaderReflection::GetConstantBufferByName (d3d12shader.h)
description: Gets a constant buffer by name.
helpviewer_keywords: ["GetConstantBufferByName","GetConstantBufferByName method","GetConstantBufferByName method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetConstantBufferByName method","ID3D12ShaderReflection.GetConstantBufferByName","ID3D12ShaderReflection::GetConstantBufferByName","d3d12shader/ID3D12ShaderReflection::GetConstantBufferByName","direct3d12.id3d12shaderreflection_getconstantbufferbyname"]
old-location: direct3d12\id3d12shaderreflection_getconstantbufferbyname.htm
tech.root: direct3d12
ms.assetid: C8BE8C17-2B5A-45AB-8C39-778FFFA78992
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method, GetConstantBufferByName method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetConstantBufferByName method, ID3D12ShaderReflection.GetConstantBufferByName, ID3D12ShaderReflection::GetConstantBufferByName, d3d12shader/ID3D12ShaderReflection::GetConstantBufferByName, direct3d12.id3d12shaderreflection_getconstantbufferbyname
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
 - ID3D12ShaderReflection::GetConstantBufferByName
 - d3d12shader/ID3D12ShaderReflection::GetConstantBufferByName
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
 - ID3D12ShaderReflection.GetConstantBufferByName
---

# ID3D12ShaderReflection::GetConstantBufferByName


## -description

Gets a constant buffer by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer Interface</a>).

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader.
        A shader can use one or more constant buffers.
        For best performance, separate constants into buffers based on the frequency they are updated.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>