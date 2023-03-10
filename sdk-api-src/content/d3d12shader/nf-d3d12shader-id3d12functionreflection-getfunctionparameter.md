---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetFunctionParameter
title: ID3D12FunctionReflection::GetFunctionParameter (d3d12shader.h)
description: Gets the function parameter reflector. (ID3D12FunctionReflection.GetFunctionParameter)
helpviewer_keywords: ["GetFunctionParameter","GetFunctionParameter method","GetFunctionParameter method","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","GetFunctionParameter method","ID3D12FunctionReflection.GetFunctionParameter","ID3D12FunctionReflection::GetFunctionParameter","d3d12shader/ID3D12FunctionReflection::GetFunctionParameter","direct3d12.id3d12functionreflection_getfunctionparameter"]
old-location: direct3d12\id3d12functionreflection_getfunctionparameter.htm
tech.root: direct3d12
ms.assetid: 88372A4E-596E-41F9-9FF4-9FD7E7F351DA
ms.date: 12/05/2018
ms.keywords: GetFunctionParameter, GetFunctionParameter method, GetFunctionParameter method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetFunctionParameter method, ID3D12FunctionReflection.GetFunctionParameter, ID3D12FunctionReflection::GetFunctionParameter, d3d12shader/ID3D12FunctionReflection::GetFunctionParameter, direct3d12.id3d12functionreflection_getfunctionparameter
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
 - ID3D12FunctionReflection::GetFunctionParameter
 - d3d12shader/ID3D12FunctionReflection::GetFunctionParameter
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
 - ID3D12FunctionReflection.GetFunctionParameter
---

# ID3D12FunctionReflection::GetFunctionParameter


## -description

Gets the function parameter reflector.

## -parameters

### -param ParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the function parameter reflector to retrieve.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection">ID3D12FunctionParameterReflection</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection">ID3D12FunctionParameterReflection</a> interface that represents the function parameter reflector.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>
