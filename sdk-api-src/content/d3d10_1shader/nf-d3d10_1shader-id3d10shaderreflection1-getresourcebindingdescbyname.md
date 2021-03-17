---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetResourceBindingDescByName
title: ID3D10ShaderReflection1::GetResourceBindingDescByName (d3d10_1shader.h)
description: Gets a resource binding description by name.
helpviewer_keywords: ["60aed60b-4d08-95c5-668d-2320735171ec","GetResourceBindingDescByName","GetResourceBindingDescByName method [Direct3D 10]","GetResourceBindingDescByName method [Direct3D 10]","ID3D10ShaderReflection1 interface","ID3D10ShaderReflection1 interface [Direct3D 10]","GetResourceBindingDescByName method","ID3D10ShaderReflection1.GetResourceBindingDescByName","ID3D10ShaderReflection1::GetResourceBindingDescByName","d3d10_1shader/ID3D10ShaderReflection1::GetResourceBindingDescByName","direct3d10.id3d10shaderreflection1_getresourcebindingdescbyname"]
old-location: direct3d10\id3d10shaderreflection1_getresourcebindingdescbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getresourcebindingdescbyname.htm
ms.date: 12/05/2018
ms.keywords: 60aed60b-4d08-95c5-668d-2320735171ec, GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 10], GetResourceBindingDescByName method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetResourceBindingDescByName method, ID3D10ShaderReflection1.GetResourceBindingDescByName, ID3D10ShaderReflection1::GetResourceBindingDescByName, d3d10_1shader/ID3D10ShaderReflection1::GetResourceBindingDescByName, direct3d10.id3d10shaderreflection1_getresourcebindingdescbyname
req.header: d3d10_1shader.h
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
 - ID3D10ShaderReflection1::GetResourceBindingDescByName
 - d3d10_1shader/ID3D10ShaderReflection1::GetResourceBindingDescByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1Shader.h
api_name:
 - ID3D10ShaderReflection1.GetResourceBindingDescByName
---

# ID3D10ShaderReflection1::GetResourceBindingDescByName


## -description

Gets a resource binding description by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a>*</b>

A pointer to a string containing the variable name.

### -param pDesc

Type: <b><a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_shader_input_bind_desc">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

Pointer to a <a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_shader_input_bind_desc">D3D10_SHADER_INPUT_BIND_DESC</a> structure that will be populated with resource binding information.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>