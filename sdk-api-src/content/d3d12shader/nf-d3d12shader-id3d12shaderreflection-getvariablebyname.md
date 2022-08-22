---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetVariableByName
title: ID3D12ShaderReflection::GetVariableByName (d3d12shader.h)
description: Gets a variable by name. (ID3D12ShaderReflection.GetVariableByName)
helpviewer_keywords: ["GetVariableByName","GetVariableByName method","GetVariableByName method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetVariableByName method","ID3D12ShaderReflection.GetVariableByName","ID3D12ShaderReflection::GetVariableByName","d3d12shader/ID3D12ShaderReflection::GetVariableByName","direct3d12.id3d12shaderreflection_getvariablebyname"]
old-location: direct3d12\id3d12shaderreflection_getvariablebyname.htm
tech.root: direct3d12
ms.assetid: E79DACF1-2C89-42BB-BB04-DFA8280987C7
ms.date: 12/05/2018
ms.keywords: GetVariableByName, GetVariableByName method, GetVariableByName method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetVariableByName method, ID3D12ShaderReflection.GetVariableByName, ID3D12ShaderReflection::GetVariableByName, d3d12shader/ID3D12ShaderReflection::GetVariableByName, direct3d12.id3d12shaderreflection_getvariablebyname
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
 - ID3D12ShaderReflection::GetVariableByName
 - d3d12shader/ID3D12ShaderReflection::GetVariableByName
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
 - ID3D12ShaderReflection.GetVariableByName
---

# ID3D12ShaderReflection::GetVariableByName


## -description

Gets a variable by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A pointer to a string containing the variable name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable</a>*</b>

Returns a <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable Interface</a> interface.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>
