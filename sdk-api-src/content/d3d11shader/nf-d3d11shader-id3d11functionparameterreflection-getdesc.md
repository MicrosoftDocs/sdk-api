---
UID: NF:d3d11shader.ID3D11FunctionParameterReflection.GetDesc
title: ID3D11FunctionParameterReflection::GetDesc (d3d11shader.h)
description: Fills the parameter descriptor structure for the function's parameter. (ID3D11FunctionParameterReflection.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11FunctionParameterReflection interface","ID3D11FunctionParameterReflection interface [Direct3D 11]","GetDesc method","ID3D11FunctionParameterReflection.GetDesc","ID3D11FunctionParameterReflection::GetDesc","d3d11shader/ID3D11FunctionParameterReflection::GetDesc","direct3d11.id3d11functionparameterreflection_getdesc"]
old-location: direct3d11\id3d11functionparameterreflection_getdesc.htm
tech.root: direct3d11
ms.assetid: 54755DEE-B865-4C9C-A38F-52749037DBBF
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11FunctionParameterReflection interface, ID3D11FunctionParameterReflection interface [Direct3D 11],GetDesc method, ID3D11FunctionParameterReflection.GetDesc, ID3D11FunctionParameterReflection::GetDesc, d3d11shader/ID3D11FunctionParameterReflection::GetDesc, direct3d11.id3d11functionparameterreflection_getdesc
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
 - ID3D11FunctionParameterReflection::GetDesc
 - d3d11shader/ID3D11FunctionParameterReflection::GetDesc
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
 - ID3D11FunctionParameterReflection.GetDesc
---

# ID3D11FunctionParameterReflection::GetDesc


## -description

Fills the parameter descriptor structure for the function's parameter.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a> structure that receives a description of the function's parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionparameterreflection">ID3D11FunctionParameterReflection</a>
