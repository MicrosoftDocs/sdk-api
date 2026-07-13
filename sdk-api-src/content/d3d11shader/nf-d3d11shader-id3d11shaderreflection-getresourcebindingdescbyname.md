---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetResourceBindingDescByName
title: ID3D11ShaderReflection::GetResourceBindingDescByName (d3d11shader.h)
description: Get a description of how a resource is bound to a shader. (ID3D11ShaderReflection.GetResourceBindingDescByName)
helpviewer_keywords: ["70b00d95-7ff3-a94d-2a18-469be48c36b3","GetResourceBindingDescByName","GetResourceBindingDescByName method [Direct3D 11]","GetResourceBindingDescByName method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetResourceBindingDescByName method","ID3D11ShaderReflection.GetResourceBindingDescByName","ID3D11ShaderReflection::GetResourceBindingDescByName","d3d11shader/ID3D11ShaderReflection::GetResourceBindingDescByName","direct3d11.id3d11shaderreflection_getresourcebindingdescbyname"]
old-location: direct3d11\id3d11shaderreflection_getresourcebindingdescbyname.htm
tech.root: direct3d11
ms.assetid: b4bddcc0-c2fd-4dac-b999-cfbe1d318777
ms.date: 12/05/2018
ms.keywords: 70b00d95-7ff3-a94d-2a18-469be48c36b3, GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 11], GetResourceBindingDescByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetResourceBindingDescByName method, ID3D11ShaderReflection.GetResourceBindingDescByName, ID3D11ShaderReflection::GetResourceBindingDescByName, d3d11shader/ID3D11ShaderReflection::GetResourceBindingDescByName, direct3d11.id3d11shaderreflection_getresourcebindingdescbyname
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
 - ID3D11ShaderReflection::GetResourceBindingDescByName
 - d3d11shader/ID3D11ShaderReflection::GetResourceBindingDescByName
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
 - ID3D11ShaderReflection.GetResourceBindingDescByName
---

# ID3D11ShaderReflection::GetResourceBindingDescByName


## -description

Get a description of how a resource is bound to a shader.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name of the resource.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_shader_input_bind_desc">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_shader_input_bind_desc">D3D11_SHADER_INPUT_BIND_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDescByName</b> gets information about how one resource in the set is bound as an input to the shader. The  <i>Name</i> parameter specifies the name of the resource.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
