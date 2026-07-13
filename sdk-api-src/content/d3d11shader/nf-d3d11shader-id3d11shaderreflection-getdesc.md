---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetDesc
title: ID3D11ShaderReflection::GetDesc (d3d11shader.h)
description: Get a shader description. (ID3D11ShaderReflection.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetDesc method","ID3D11ShaderReflection.GetDesc","ID3D11ShaderReflection::GetDesc","af085ff0-7b2a-4e9e-cdad-aaa679defcc1","d3d11shader/ID3D11ShaderReflection::GetDesc","direct3d11.id3d11shaderreflection_getdesc"]
old-location: direct3d11\id3d11shaderreflection_getdesc.htm
tech.root: direct3d11
ms.assetid: 88bebd52-5da0-473e-8f26-63a82ce99938
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetDesc method, ID3D11ShaderReflection.GetDesc, ID3D11ShaderReflection::GetDesc, af085ff0-7b2a-4e9e-cdad-aaa679defcc1, d3d11shader/ID3D11ShaderReflection::GetDesc, direct3d11.id3d11shaderreflection_getdesc
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
 - ID3D11ShaderReflection::GetDesc
 - d3d11shader/ID3D11ShaderReflection::GetDesc
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
 - ID3D11ShaderReflection.GetDesc
---

# ID3D11ShaderReflection::GetDesc


## -description

Get a shader description.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_desc">D3D11_SHADER_DESC</a>*</b>

A pointer to a shader description. See <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_desc">D3D11_SHADER_DESC</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
