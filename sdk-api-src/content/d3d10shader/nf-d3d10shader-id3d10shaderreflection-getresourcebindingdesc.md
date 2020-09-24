---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetResourceBindingDesc
title: ID3D10ShaderReflection::GetResourceBindingDesc (d3d10shader.h)
description: Get a description of the resources bound to a shader.
helpviewer_keywords: ["6c7ed61d-9513-cb71-b3ae-307487d0a4eb","GetResourceBindingDesc","GetResourceBindingDesc method [Direct3D 10]","GetResourceBindingDesc method [Direct3D 10]","ID3D10ShaderReflection interface","ID3D10ShaderReflection interface [Direct3D 10]","GetResourceBindingDesc method","ID3D10ShaderReflection.GetResourceBindingDesc","ID3D10ShaderReflection::GetResourceBindingDesc","d3d10shader/ID3D10ShaderReflection::GetResourceBindingDesc","direct3d10.id3d10shaderreflection_getresourcebindingdesc"]
old-location: direct3d10\id3d10shaderreflection_getresourcebindingdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getresourcebindingdesc.htm
ms.date: 12/05/2018
ms.keywords: 6c7ed61d-9513-cb71-b3ae-307487d0a4eb, GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 10], GetResourceBindingDesc method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetResourceBindingDesc method, ID3D10ShaderReflection.GetResourceBindingDesc, ID3D10ShaderReflection::GetResourceBindingDesc, d3d10shader/ID3D10ShaderReflection::GetResourceBindingDesc, direct3d10.id3d10shaderreflection_getresourcebindingdesc
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
 - ID3D10ShaderReflection::GetResourceBindingDesc
 - d3d10shader/ID3D10ShaderReflection::GetResourceBindingDesc
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
 - ID3D10ShaderReflection.GetResourceBindingDesc
---

# ID3D10ShaderReflection::GetResourceBindingDesc


## -description

Get a description of the resources bound to a shader.

## -parameters

### -param ResourceIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based resource index.

### -param pDesc [in]

Type: <b><a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_shader_input_bind_desc">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_shader_input_bind_desc">D3D10_SHADER_INPUT_BIND_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. This API gets a list of the resources that are bound as inputs to the shader.

## -see-also

<a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection">ID3D10ShaderReflection Interface</a>