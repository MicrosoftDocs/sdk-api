---
UID: NF:d3d12shader.ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex
title: ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex (d3d12shader.h)
description: Gets a shader-reflection variable by index.
helpviewer_keywords: ["GetVariableByIndex","GetVariableByIndex method","GetVariableByIndex method","ID3D12ShaderReflectionConstantBuffer interface","ID3D12ShaderReflectionConstantBuffer interface","GetVariableByIndex method","ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex","ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex","d3d12shader/ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex","direct3d12.id3d12shaderreflectionconstantbuffer_getvariablebyindex"]
old-location: direct3d12\id3d12shaderreflectionconstantbuffer_getvariablebyindex.htm
tech.root: direct3d12
ms.assetid: F7083A4D-ADD4-4C6F-A031-ABF16A3C351C
ms.date: 12/05/2018
ms.keywords: GetVariableByIndex, GetVariableByIndex method, GetVariableByIndex method,ID3D12ShaderReflectionConstantBuffer interface, ID3D12ShaderReflectionConstantBuffer interface,GetVariableByIndex method, ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex, ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex, d3d12shader/ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex, direct3d12.id3d12shaderreflectionconstantbuffer_getvariablebyindex
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
 - ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex
 - d3d12shader/ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex
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
 - ID3D12ShaderReflectionConstantBuffer.GetVariableByIndex
---

# ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex


## -description

Gets a shader-reflection variable by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable</a>*</b>

A pointer to a shader-reflection variable interface (see <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable Interface</a>).

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>