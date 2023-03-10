---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetResourceBindingDesc
title: ID3D12FunctionReflection::GetResourceBindingDesc (d3d12shader.h)
description: Gets a description of how a resource is bound to a function. (ID3D12FunctionReflection.GetResourceBindingDesc)
helpviewer_keywords: ["GetResourceBindingDesc","GetResourceBindingDesc method","GetResourceBindingDesc method","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","GetResourceBindingDesc method","ID3D12FunctionReflection.GetResourceBindingDesc","ID3D12FunctionReflection::GetResourceBindingDesc","d3d12shader/ID3D12FunctionReflection::GetResourceBindingDesc","direct3d12.id3d12functionreflection_getresourcebindingdesc"]
old-location: direct3d12\id3d12functionreflection_getresourcebindingdesc.htm
tech.root: direct3d12
ms.assetid: DBABC959-0692-4DB9-9726-AFE6972A6B52
ms.date: 12/05/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method, GetResourceBindingDesc method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetResourceBindingDesc method, ID3D12FunctionReflection.GetResourceBindingDesc, ID3D12FunctionReflection::GetResourceBindingDesc, d3d12shader/ID3D12FunctionReflection::GetResourceBindingDesc, direct3d12.id3d12functionreflection_getresourcebindingdesc
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
 - ID3D12FunctionReflection::GetResourceBindingDesc
 - d3d12shader/ID3D12FunctionReflection::GetResourceBindingDesc
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
 - ID3D12FunctionReflection.GetResourceBindingDesc
---

# ID3D12FunctionReflection::GetResourceBindingDesc


## -description

Gets a description of how a resource is bound to a function.

## -parameters

### -param ResourceIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based resource index.

### -param pDesc [out]

Type: <b><a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc">D3D12_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="/windows/win32/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc">D3D12_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets info about how one resource in the set is bound as an input to the shader. 
          The <i>ResourceIndex</i> parameter specifies the index for the resource.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>
