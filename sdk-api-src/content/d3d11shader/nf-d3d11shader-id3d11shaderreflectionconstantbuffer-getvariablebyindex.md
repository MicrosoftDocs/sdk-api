---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex
title: ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex (d3d11shader.h)
description: The ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex (d3d11shader.h) method gets a shader-reflection variable by index.
helpviewer_keywords: ["45c0f056-8446-d61d-24b8-31ff2f2a92ff","GetVariableByIndex","GetVariableByIndex method [Direct3D 11]","GetVariableByIndex method [Direct3D 11]","ID3D11ShaderReflectionConstantBuffer interface","ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11]","GetVariableByIndex method","ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex","ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex","d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex","direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyindex"]
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getvariablebyindex.htm
tech.root: direct3d11
ms.assetid: fafdf040-223c-4e69-95b6-05c62ea8ff52
ms.date: 08/10/2022
ms.keywords: 45c0f056-8446-d61d-24b8-31ff2f2a92ff, GetVariableByIndex, GetVariableByIndex method [Direct3D 11], GetVariableByIndex method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetVariableByIndex method, ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex, ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex, direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyindex
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
 - ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex
 - d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex
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
 - ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex
---

# ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex


## -description

Get a shader-reflection variable by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable</a>*</b>

A pointer to a shader-reflection variable interface (see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable Interface</a>).

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer Interface</a>