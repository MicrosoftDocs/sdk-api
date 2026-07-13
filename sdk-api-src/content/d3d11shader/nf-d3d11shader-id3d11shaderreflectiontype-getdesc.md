---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.GetDesc
title: ID3D11ShaderReflectionType::GetDesc (d3d11shader.h)
description: Get the description of a shader-reflection-variable type. (ID3D11ShaderReflectionType.GetDesc)
helpviewer_keywords: ["0828a5c8-51bc-2665-51f3-1125bd152a6e","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11ShaderReflectionType interface","ID3D11ShaderReflectionType interface [Direct3D 11]","GetDesc method","ID3D11ShaderReflectionType.GetDesc","ID3D11ShaderReflectionType::GetDesc","d3d11shader/ID3D11ShaderReflectionType::GetDesc","direct3d11.id3d11shaderreflectiontype_getdesc"]
old-location: direct3d11\id3d11shaderreflectiontype_getdesc.htm
tech.root: direct3d11
ms.assetid: 96296270-fcca-4843-bd0a-78c7f87136e5
ms.date: 12/05/2018
ms.keywords: 0828a5c8-51bc-2665-51f3-1125bd152a6e, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflectionType interface, ID3D11ShaderReflectionType interface [Direct3D 11],GetDesc method, ID3D11ShaderReflectionType.GetDesc, ID3D11ShaderReflectionType::GetDesc, d3d11shader/ID3D11ShaderReflectionType::GetDesc, direct3d11.id3d11shaderreflectiontype_getdesc
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
 - ID3D11ShaderReflectionType::GetDesc
 - d3d11shader/ID3D11ShaderReflectionType::GetDesc
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
 - ID3D11ShaderReflectionType.GetDesc
---

# ID3D11ShaderReflectionType::GetDesc


## -description

Get the description of a shader-reflection-variable type.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_type_desc">D3D11_SHADER_TYPE_DESC</a>*</b>

A pointer to a shader-type description (see <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_type_desc">D3D11_SHADER_TYPE_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>
