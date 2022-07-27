---
UID: NF:d3d12shader.ID3D12FunctionParameterReflection.GetDesc
title: ID3D12FunctionParameterReflection::GetDesc (d3d12shader.h)
description: Fills the parameter descriptor structure for the function's parameter. (ID3D12FunctionParameterReflection.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method","GetDesc method","ID3D12FunctionParameterReflection interface","ID3D12FunctionParameterReflection interface","GetDesc method","ID3D12FunctionParameterReflection.GetDesc","ID3D12FunctionParameterReflection::GetDesc","d3d12shader/ID3D12FunctionParameterReflection::GetDesc","direct3d12.id3d12functionparameterreflection_getdesc"]
old-location: direct3d12\id3d12functionparameterreflection_getdesc.htm
tech.root: direct3d12
ms.assetid: E10ACB2E-EF77-4C71-A5C7-CEFA31218091
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12FunctionParameterReflection interface, ID3D12FunctionParameterReflection interface,GetDesc method, ID3D12FunctionParameterReflection.GetDesc, ID3D12FunctionParameterReflection::GetDesc, d3d12shader/ID3D12FunctionParameterReflection::GetDesc, direct3d12.id3d12functionparameterreflection_getdesc
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
 - ID3D12FunctionParameterReflection::GetDesc
 - d3d12shader/ID3D12FunctionParameterReflection::GetDesc
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
 - ID3D12FunctionParameterReflection.GetDesc
---

# ID3D12FunctionParameterReflection::GetDesc


## -description

Fills the parameter descriptor structure for the function's parameter.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc">D3D12_PARAMETER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc">D3D12_PARAMETER_DESC</a> structure that receives a description of the function's parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection">ID3D12FunctionParameterReflection</a>
