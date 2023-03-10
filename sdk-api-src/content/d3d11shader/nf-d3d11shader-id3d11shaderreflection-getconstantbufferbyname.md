---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetConstantBufferByName
title: ID3D11ShaderReflection::GetConstantBufferByName (d3d11shader.h)
description: Get a constant buffer by name. (ID3D11ShaderReflection.GetConstantBufferByName)
helpviewer_keywords: ["GetConstantBufferByName","GetConstantBufferByName method [Direct3D 11]","GetConstantBufferByName method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetConstantBufferByName method","ID3D11ShaderReflection.GetConstantBufferByName","ID3D11ShaderReflection::GetConstantBufferByName","d3d11shader/ID3D11ShaderReflection::GetConstantBufferByName","d50e9f46-8347-fa35-807d-0bbcf91adf69","direct3d11.id3d11shaderreflection_getconstantbufferbyname"]
old-location: direct3d11\id3d11shaderreflection_getconstantbufferbyname.htm
tech.root: direct3d11
ms.assetid: 6b0e16c9-f45a-42d0-bd96-32dfa859b35d
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 11], GetConstantBufferByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetConstantBufferByName method, ID3D11ShaderReflection.GetConstantBufferByName, ID3D11ShaderReflection::GetConstantBufferByName, d3d11shader/ID3D11ShaderReflection::GetConstantBufferByName, d50e9f46-8347-fa35-807d-0bbcf91adf69, direct3d11.id3d11shaderreflection_getconstantbufferbyname
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
 - ID3D11ShaderReflection::GetConstantBufferByName
 - d3d11shader/ID3D11ShaderReflection::GetConstantBufferByName
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
 - ID3D11ShaderReflection.GetConstantBufferByName
---

# ID3D11ShaderReflection::GetConstantBufferByName


## -description

Get a constant buffer by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer Interface</a>).

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
