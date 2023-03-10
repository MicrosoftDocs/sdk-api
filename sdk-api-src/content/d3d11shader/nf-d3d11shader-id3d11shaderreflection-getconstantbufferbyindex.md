---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetConstantBufferByIndex
title: ID3D11ShaderReflection::GetConstantBufferByIndex (d3d11shader.h)
description: The ID3D11ShaderReflection::GetConstantBufferByIndex (d3d11shader.h) method gets a constant buffer by index.
helpviewer_keywords: ["GetConstantBufferByIndex","GetConstantBufferByIndex method [Direct3D 11]","GetConstantBufferByIndex method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetConstantBufferByIndex method","ID3D11ShaderReflection.GetConstantBufferByIndex","ID3D11ShaderReflection::GetConstantBufferByIndex","a1aee75d-6029-a494-025f-69188d4e1655","d3d11shader/ID3D11ShaderReflection::GetConstantBufferByIndex","direct3d11.id3d11shaderreflection_getconstantbufferbyindex"]
old-location: direct3d11\id3d11shaderreflection_getconstantbufferbyindex.htm
tech.root: direct3d11
ms.assetid: 6a1be6a0-0337-408d-9e31-8dd388faaf5d
ms.date: 08/10/2022
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method [Direct3D 11], GetConstantBufferByIndex method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetConstantBufferByIndex method, ID3D11ShaderReflection.GetConstantBufferByIndex, ID3D11ShaderReflection::GetConstantBufferByIndex, a1aee75d-6029-a494-025f-69188d4e1655, d3d11shader/ID3D11ShaderReflection::GetConstantBufferByIndex, direct3d11.id3d11shaderreflection_getconstantbufferbyindex
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
 - ID3D11ShaderReflection::GetConstantBufferByIndex
 - d3d11shader/ID3D11ShaderReflection::GetConstantBufferByIndex
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
 - ID3D11ShaderReflection.GetConstantBufferByIndex
---

# ID3D11ShaderReflection::GetConstantBufferByIndex


## -description

Get a constant buffer by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer Interface</a>).

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>