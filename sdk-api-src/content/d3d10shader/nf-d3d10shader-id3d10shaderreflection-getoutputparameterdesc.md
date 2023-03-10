---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetOutputParameterDesc
title: ID3D10ShaderReflection::GetOutputParameterDesc (d3d10shader.h)
description: Get an output-parameter description for a shader. (ID3D10ShaderReflection.GetOutputParameterDesc)
helpviewer_keywords: ["GetOutputParameterDesc","GetOutputParameterDesc method [Direct3D 10]","GetOutputParameterDesc method [Direct3D 10]","ID3D10ShaderReflection interface","ID3D10ShaderReflection interface [Direct3D 10]","GetOutputParameterDesc method","ID3D10ShaderReflection.GetOutputParameterDesc","ID3D10ShaderReflection::GetOutputParameterDesc","d3d10shader/ID3D10ShaderReflection::GetOutputParameterDesc","direct3d10.id3d10shaderreflection_getoutputparameterdesc","e1ba0a0a-1c0d-b2cd-1246-59c039de1f0c"]
old-location: direct3d10\id3d10shaderreflection_getoutputparameterdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getoutputparameterdesc.htm
ms.date: 12/05/2018
ms.keywords: GetOutputParameterDesc, GetOutputParameterDesc method [Direct3D 10], GetOutputParameterDesc method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetOutputParameterDesc method, ID3D10ShaderReflection.GetOutputParameterDesc, ID3D10ShaderReflection::GetOutputParameterDesc, d3d10shader/ID3D10ShaderReflection::GetOutputParameterDesc, direct3d10.id3d10shaderreflection_getoutputparameterdesc, e1ba0a0a-1c0d-b2cd-1246-59c039de1f0c
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
 - ID3D10ShaderReflection::GetOutputParameterDesc
 - d3d10shader/ID3D10ShaderReflection::GetOutputParameterDesc
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
 - ID3D10ShaderReflection.GetOutputParameterDesc
---

# ID3D10ShaderReflection::GetOutputParameterDesc


## -description

Get an output-parameter description for a shader.

## -parameters

### -param ParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based parameter index.

### -param pDesc [in]

Type: <b><a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-output-parameter description. See <a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An output-parameter description is also called a shader signature. The shader signature contains information about the output parameters such as the order or parameters, their data type, and a parameter semantic.

## -see-also

<a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection">ID3D10ShaderReflection Interface</a>
