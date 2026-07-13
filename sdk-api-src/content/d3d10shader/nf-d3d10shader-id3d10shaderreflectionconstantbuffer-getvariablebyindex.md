---
UID: NF:d3d10shader.ID3D10ShaderReflectionConstantBuffer.GetVariableByIndex
title: ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex (d3d10shader.h)
description: The ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex (d3d10shader.h) method gets a shader-reflection variable by index.
helpviewer_keywords: ["GetVariableByIndex","GetVariableByIndex method [Direct3D 10]","GetVariableByIndex method [Direct3D 10]","ID3D10ShaderReflectionConstantBuffer interface","ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10]","GetVariableByIndex method","ID3D10ShaderReflectionConstantBuffer.GetVariableByIndex","ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex","d3d10shader/ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex","dc3115ea-2cdd-68c8-a77f-883ae86bf1a4","direct3d10.id3d10shaderreflectionconstantbuffer_getvariablebyindex"]
old-location: direct3d10\id3d10shaderreflectionconstantbuffer_getvariablebyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionconstantbuffer_getvariablebyindex.htm
ms.date: 08/10/2022
ms.keywords: GetVariableByIndex, GetVariableByIndex method [Direct3D 10], GetVariableByIndex method [Direct3D 10],ID3D10ShaderReflectionConstantBuffer interface, ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10],GetVariableByIndex method, ID3D10ShaderReflectionConstantBuffer.GetVariableByIndex, ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex, d3d10shader/ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex, dc3115ea-2cdd-68c8-a77f-883ae86bf1a4, direct3d10.id3d10shaderreflectionconstantbuffer_getvariablebyindex
req.header: d3d10shader.h
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
 - ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex
 - d3d10shader/ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Shader.h
api_name:
 - ID3D10ShaderReflectionConstantBuffer.GetVariableByIndex
---

# ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex


## -description

Get a shader-reflection variable by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionvariable">ID3D10ShaderReflectionVariable</a>*</b>

A pointer to a shader-reflection variable interface (see <a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionvariable">ID3D10ShaderReflectionVariable Interface</a>).

## -see-also

<a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer">ID3D10ShaderReflectionConstantBuffer Interface</a>