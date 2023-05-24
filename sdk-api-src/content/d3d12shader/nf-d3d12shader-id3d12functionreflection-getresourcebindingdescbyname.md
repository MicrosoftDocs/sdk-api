---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetResourceBindingDescByName
title: ID3D12FunctionReflection::GetResourceBindingDescByName (d3d12shader.h)
description: Gets a description of how a resource is bound to a function. (ID3D12FunctionReflection.GetResourceBindingDescByName)
helpviewer_keywords: ["GetResourceBindingDescByName","GetResourceBindingDescByName method","GetResourceBindingDescByName method","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","GetResourceBindingDescByName method","ID3D12FunctionReflection.GetResourceBindingDescByName","ID3D12FunctionReflection::GetResourceBindingDescByName","d3d12shader/ID3D12FunctionReflection::GetResourceBindingDescByName","direct3d12.id3d12functionreflection_getresourcebindingdescbyname"]
old-location: direct3d12\id3d12functionreflection_getresourcebindingdescbyname.htm
tech.root: direct3d12
ms.assetid: CF13496F-4317-4FFF-85CA-08FC64E320F4
ms.date: 12/05/2018
ms.keywords: GetResourceBindingDescByName, GetResourceBindingDescByName method, GetResourceBindingDescByName method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetResourceBindingDescByName method, ID3D12FunctionReflection.GetResourceBindingDescByName, ID3D12FunctionReflection::GetResourceBindingDescByName, d3d12shader/ID3D12FunctionReflection::GetResourceBindingDescByName, direct3d12.id3d12functionreflection_getresourcebindingdescbyname
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
 - ID3D12FunctionReflection::GetResourceBindingDescByName
 - d3d12shader/ID3D12FunctionReflection::GetResourceBindingDescByName
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
 - ID3D12FunctionReflection.GetResourceBindingDescByName
---

# ID3D12FunctionReflection::GetResourceBindingDescByName


## -description

Gets a description of how a resource is bound to a function.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name of the resource.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc">D3D12_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc">D3D12_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDescByName</b> gets info about how one resource in the set is bound as an input to the shader. The  <i>Name</i> parameter specifies the name of the resource.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>
