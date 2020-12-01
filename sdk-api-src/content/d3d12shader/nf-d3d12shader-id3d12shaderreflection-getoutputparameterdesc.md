---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetOutputParameterDesc
title: ID3D12ShaderReflection::GetOutputParameterDesc (d3d12shader.h)
description: Gets an output-parameter description for a shader.
helpviewer_keywords: ["GetOutputParameterDesc","GetOutputParameterDesc method","GetOutputParameterDesc method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetOutputParameterDesc method","ID3D12ShaderReflection.GetOutputParameterDesc","ID3D12ShaderReflection::GetOutputParameterDesc","d3d12shader/ID3D12ShaderReflection::GetOutputParameterDesc","direct3d12.id3d12shaderreflection_getoutputparameterdesc"]
old-location: direct3d12\id3d12shaderreflection_getoutputparameterdesc.htm
tech.root: direct3d12
ms.assetid: 6B767F3A-54A7-40F0-B9A9-FD69FA07C689
ms.date: 12/05/2018
ms.keywords: GetOutputParameterDesc, GetOutputParameterDesc method, GetOutputParameterDesc method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetOutputParameterDesc method, ID3D12ShaderReflection.GetOutputParameterDesc, ID3D12ShaderReflection::GetOutputParameterDesc, d3d12shader/ID3D12ShaderReflection::GetOutputParameterDesc, direct3d12.id3d12shaderreflection_getoutputparameterdesc
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
 - ID3D12ShaderReflection::GetOutputParameterDesc
 - d3d12shader/ID3D12ShaderReflection::GetOutputParameterDesc
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
 - ID3D12ShaderReflection.GetOutputParameterDesc
---

# ID3D12ShaderReflection::GetOutputParameterDesc


## -description

Gets an output-parameter description for a shader.

## -parameters

### -param ParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based parameter index.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc">D3D12_SIGNATURE_PARAMETER_DESC</a>*</b>

A shader-output-parameter description, as a pointer to a <a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc">D3D12_SIGNATURE_PARAMETER_DESC</a> structure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

An output-parameter description is also called a shader signature. The shader signature contains information about the output parameters such as the order or parameters, their data type, and a parameter semantic.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>