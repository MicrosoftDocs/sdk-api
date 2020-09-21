---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetPatchConstantParameterDesc
title: ID3D11ShaderReflection::GetPatchConstantParameterDesc (d3d11shader.h)
description: Get a patch-constant parameter description for a shader.
helpviewer_keywords: ["GetPatchConstantParameterDesc","GetPatchConstantParameterDesc method [Direct3D 11]","GetPatchConstantParameterDesc method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetPatchConstantParameterDesc method","ID3D11ShaderReflection.GetPatchConstantParameterDesc","ID3D11ShaderReflection::GetPatchConstantParameterDesc","a1d3c039-54af-ae32-0c02-c7d90751aacc","d3d11shader/ID3D11ShaderReflection::GetPatchConstantParameterDesc","direct3d11.id3d11shaderreflection_getpatchconstantparameterdesc"]
old-location: direct3d11\id3d11shaderreflection_getpatchconstantparameterdesc.htm
tech.root: direct3d11
ms.assetid: 91a1a3ac-1dd4-4d91-aaea-196a99d5d684
ms.date: 12/05/2018
ms.keywords: GetPatchConstantParameterDesc, GetPatchConstantParameterDesc method [Direct3D 11], GetPatchConstantParameterDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetPatchConstantParameterDesc method, ID3D11ShaderReflection.GetPatchConstantParameterDesc, ID3D11ShaderReflection::GetPatchConstantParameterDesc, a1d3c039-54af-ae32-0c02-c7d90751aacc, d3d11shader/ID3D11ShaderReflection::GetPatchConstantParameterDesc, direct3d11.id3d11shaderreflection_getpatchconstantparameterdesc
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
 - ID3D11ShaderReflection::GetPatchConstantParameterDesc
 - d3d11shader/ID3D11ShaderReflection::GetPatchConstantParameterDesc
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
 - ID3D11ShaderReflection.GetPatchConstantParameterDesc
---

# ID3D11ShaderReflection::GetPatchConstantParameterDesc


## -description

Get a patch-constant parameter description for a shader.

## -parameters

### -param ParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based parameter index.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_signature_parameter_desc">D3D11_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-input-signature description. See <a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_signature_parameter_desc">D3D11_SIGNATURE_PARAMETER_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>