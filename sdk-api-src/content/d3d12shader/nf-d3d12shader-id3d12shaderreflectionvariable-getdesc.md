---
UID: NF:d3d12shader.ID3D12ShaderReflectionVariable.GetDesc
title: ID3D12ShaderReflectionVariable::GetDesc (d3d12shader.h)
description: Gets a shader-variable description.
helpviewer_keywords: ["GetDesc","GetDesc method","GetDesc method","ID3D12ShaderReflectionVariable interface","ID3D12ShaderReflectionVariable interface","GetDesc method","ID3D12ShaderReflectionVariable.GetDesc","ID3D12ShaderReflectionVariable::GetDesc","d3d12shader/ID3D12ShaderReflectionVariable::GetDesc","direct3d12.id3d12shaderreflectionvariable_getdesc"]
old-location: direct3d12\id3d12shaderreflectionvariable_getdesc.htm
tech.root: direct3d12
ms.assetid: 21CF98AF-5645-4059-992A-FFF778576C93
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,GetDesc method, ID3D12ShaderReflectionVariable.GetDesc, ID3D12ShaderReflectionVariable::GetDesc, d3d12shader/ID3D12ShaderReflectionVariable::GetDesc, direct3d12.id3d12shaderreflectionvariable_getdesc
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
 - ID3D12ShaderReflectionVariable::GetDesc
 - d3d12shader/ID3D12ShaderReflectionVariable::GetDesc
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
 - ID3D12ShaderReflectionVariable.GetDesc
---

# ID3D12ShaderReflectionVariable::GetDesc


## -description

Gets a shader-variable description.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc">D3D12_SHADER_VARIABLE_DESC</a>*</b>

A pointer to a shader-variable description (see <a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc">D3D12_SHADER_VARIABLE_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This method can be used to determine if the <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable Interface</a> is valid, the method returns <b>E_FAIL</b> when the variable is not valid.
        

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable</a>