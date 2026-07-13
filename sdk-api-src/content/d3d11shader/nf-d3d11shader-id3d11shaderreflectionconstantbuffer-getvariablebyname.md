---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetVariableByName
title: ID3D11ShaderReflectionConstantBuffer::GetVariableByName (d3d11shader.h)
description: Get a shader-reflection variable by name. (ID3D11ShaderReflectionConstantBuffer.GetVariableByName)
helpviewer_keywords: ["613cfca7-07e9-dcae-c494-e5cdf1002b8c","GetVariableByName","GetVariableByName method [Direct3D 11]","GetVariableByName method [Direct3D 11]","ID3D11ShaderReflectionConstantBuffer interface","ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11]","GetVariableByName method","ID3D11ShaderReflectionConstantBuffer.GetVariableByName","ID3D11ShaderReflectionConstantBuffer::GetVariableByName","d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByName","direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyname"]
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getvariablebyname.htm
tech.root: direct3d11
ms.assetid: daa14557-0987-4498-a2f5-428497805eca
ms.date: 12/05/2018
ms.keywords: 613cfca7-07e9-dcae-c494-e5cdf1002b8c, GetVariableByName, GetVariableByName method [Direct3D 11], GetVariableByName method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetVariableByName method, ID3D11ShaderReflectionConstantBuffer.GetVariableByName, ID3D11ShaderReflectionConstantBuffer::GetVariableByName, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByName, direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyname
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
 - ID3D11ShaderReflectionConstantBuffer::GetVariableByName
 - d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByName
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
 - ID3D11ShaderReflectionConstantBuffer.GetVariableByName
---

# ID3D11ShaderReflectionConstantBuffer::GetVariableByName


## -description

Get a shader-reflection variable by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Variable name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable</a>*</b>

Returns a sentinel object (end of list marker). To determine if GetVariableByName successfully completed, call <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc">ID3D11ShaderReflectionVariable::GetDesc</a> and check the returned <b>HRESULT</b>; any return value other than success means that GetVariableByName failed.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer Interface</a>
