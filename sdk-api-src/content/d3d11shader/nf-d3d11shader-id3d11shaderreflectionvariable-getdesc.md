---
UID: NF:d3d11shader.ID3D11ShaderReflectionVariable.GetDesc
title: ID3D11ShaderReflectionVariable::GetDesc (d3d11shader.h)
description: Get a shader-variable description. (ID3D11ShaderReflectionVariable.GetDesc)
helpviewer_keywords: ["6ae72773-659b-8911-13a0-cbaa49ed3c83","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11ShaderReflectionVariable interface","ID3D11ShaderReflectionVariable interface [Direct3D 11]","GetDesc method","ID3D11ShaderReflectionVariable.GetDesc","ID3D11ShaderReflectionVariable::GetDesc","d3d11shader/ID3D11ShaderReflectionVariable::GetDesc","direct3d11.id3d11shaderreflectionvariable_getdesc"]
old-location: direct3d11\id3d11shaderreflectionvariable_getdesc.htm
tech.root: direct3d11
ms.assetid: a384e172-763f-4f4c-b6fb-f657fa31e5ee
ms.date: 12/05/2018
ms.keywords: 6ae72773-659b-8911-13a0-cbaa49ed3c83, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflectionVariable interface, ID3D11ShaderReflectionVariable interface [Direct3D 11],GetDesc method, ID3D11ShaderReflectionVariable.GetDesc, ID3D11ShaderReflectionVariable::GetDesc, d3d11shader/ID3D11ShaderReflectionVariable::GetDesc, direct3d11.id3d11shaderreflectionvariable_getdesc
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
 - ID3D11ShaderReflectionVariable::GetDesc
 - d3d11shader/ID3D11ShaderReflectionVariable::GetDesc
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
 - ID3D11ShaderReflectionVariable.GetDesc
---

# ID3D11ShaderReflectionVariable::GetDesc


## -description

Get a shader-variable description.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc">D3D11_SHADER_VARIABLE_DESC</a>*</b>

A pointer to a shader-variable description (see <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc">D3D11_SHADER_VARIABLE_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method can be used to determine if the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable Interface</a> is valid, the method returns <b>E_FAIL</b> when the variable is not valid.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable Interface</a>
