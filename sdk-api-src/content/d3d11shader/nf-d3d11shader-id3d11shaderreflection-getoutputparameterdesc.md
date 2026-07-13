---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetOutputParameterDesc
title: ID3D11ShaderReflection::GetOutputParameterDesc (d3d11shader.h)
description: Get an output-parameter description for a shader. (ID3D11ShaderReflection.GetOutputParameterDesc)
helpviewer_keywords: ["GetOutputParameterDesc","GetOutputParameterDesc method [Direct3D 11]","GetOutputParameterDesc method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetOutputParameterDesc method","ID3D11ShaderReflection.GetOutputParameterDesc","ID3D11ShaderReflection::GetOutputParameterDesc","c79e62b5-e5fb-6a0f-07c6-439fa953073b","d3d11shader/ID3D11ShaderReflection::GetOutputParameterDesc","direct3d11.id3d11shaderreflection_getoutputparameterdesc"]
old-location: direct3d11\id3d11shaderreflection_getoutputparameterdesc.htm
tech.root: direct3d11
ms.assetid: 7fc27fae-d17a-4247-bd79-e02956890efd
ms.date: 12/05/2018
ms.keywords: GetOutputParameterDesc, GetOutputParameterDesc method [Direct3D 11], GetOutputParameterDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetOutputParameterDesc method, ID3D11ShaderReflection.GetOutputParameterDesc, ID3D11ShaderReflection::GetOutputParameterDesc, c79e62b5-e5fb-6a0f-07c6-439fa953073b, d3d11shader/ID3D11ShaderReflection::GetOutputParameterDesc, direct3d11.id3d11shaderreflection_getoutputparameterdesc
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
 - ID3D11ShaderReflection::GetOutputParameterDesc
 - d3d11shader/ID3D11ShaderReflection::GetOutputParameterDesc
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
 - ID3D11ShaderReflection.GetOutputParameterDesc
---

# ID3D11ShaderReflection::GetOutputParameterDesc


## -description

Get an output-parameter description for a shader.

## -parameters

### -param ParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based parameter index.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_signature_parameter_desc">D3D11_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-output-parameter description. See <a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_signature_parameter_desc">D3D11_SIGNATURE_PARAMETER_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

An output-parameter description is also called a shader signature. The shader signature contains information about the output parameters such as the order or parameters, their data type, and a parameter semantic.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
