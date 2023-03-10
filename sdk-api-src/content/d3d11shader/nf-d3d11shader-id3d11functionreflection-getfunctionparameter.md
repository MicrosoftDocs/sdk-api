---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetFunctionParameter
title: ID3D11FunctionReflection::GetFunctionParameter (d3d11shader.h)
description: Gets the function parameter reflector. (ID3D11FunctionReflection.GetFunctionParameter)
helpviewer_keywords: ["GetFunctionParameter","GetFunctionParameter method [Direct3D 11]","GetFunctionParameter method [Direct3D 11]","ID3D11FunctionReflection interface","ID3D11FunctionReflection interface [Direct3D 11]","GetFunctionParameter method","ID3D11FunctionReflection.GetFunctionParameter","ID3D11FunctionReflection::GetFunctionParameter","d3d11shader/ID3D11FunctionReflection::GetFunctionParameter","direct3d11.id3d11functionreflection_getfunctionparameter"]
old-location: direct3d11\id3d11functionreflection_getfunctionparameter.htm
tech.root: direct3d11
ms.assetid: DA2A3226-7204-4722-BCA0-74B38793A319
ms.date: 12/05/2018
ms.keywords: GetFunctionParameter, GetFunctionParameter method [Direct3D 11], GetFunctionParameter method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetFunctionParameter method, ID3D11FunctionReflection.GetFunctionParameter, ID3D11FunctionReflection::GetFunctionParameter, d3d11shader/ID3D11FunctionReflection::GetFunctionParameter, direct3d11.id3d11functionreflection_getfunctionparameter
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
 - ID3D11FunctionReflection::GetFunctionParameter
 - d3d11shader/ID3D11FunctionReflection::GetFunctionParameter
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
 - ID3D11FunctionReflection.GetFunctionParameter
---

# ID3D11FunctionReflection::GetFunctionParameter


## -description

Gets the function parameter reflector.

## -parameters

### -param ParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the function parameter reflector to retrieve.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionparameterreflection">ID3D11FunctionParameterReflection</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionparameterreflection">ID3D11FunctionParameterReflection</a> interface that represents the function parameter reflector.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionreflection">ID3D11FunctionReflection</a>
