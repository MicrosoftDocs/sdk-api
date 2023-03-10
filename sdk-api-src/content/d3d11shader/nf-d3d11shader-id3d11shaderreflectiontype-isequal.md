---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.IsEqual
title: ID3D11ShaderReflectionType::IsEqual (d3d11shader.h)
description: Indicates whether two ID3D11ShaderReflectionType Interface pointers have the same underlying type.
helpviewer_keywords: ["5ed95f14-be4b-bff2-83ce-cbf5f239bf3b","ID3D11ShaderReflectionType interface [Direct3D 11]","IsEqual method","ID3D11ShaderReflectionType.IsEqual","ID3D11ShaderReflectionType::IsEqual","IsEqual","IsEqual method [Direct3D 11]","IsEqual method [Direct3D 11]","ID3D11ShaderReflectionType interface","d3d11shader/ID3D11ShaderReflectionType::IsEqual","direct3d11.id3d11shaderreflectiontype_isequal"]
old-location: direct3d11\id3d11shaderreflectiontype_isequal.htm
tech.root: direct3d11
ms.assetid: 99a70bf3-bbd1-49a1-a59f-c35f7236b16f
ms.date: 12/05/2018
ms.keywords: 5ed95f14-be4b-bff2-83ce-cbf5f239bf3b, ID3D11ShaderReflectionType interface [Direct3D 11],IsEqual method, ID3D11ShaderReflectionType.IsEqual, ID3D11ShaderReflectionType::IsEqual, IsEqual, IsEqual method [Direct3D 11], IsEqual method [Direct3D 11],ID3D11ShaderReflectionType interface, d3d11shader/ID3D11ShaderReflectionType::IsEqual, direct3d11.id3d11shaderreflectiontype_isequal
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
 - ID3D11ShaderReflectionType::IsEqual
 - d3d11shader/ID3D11ShaderReflectionType::IsEqual
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
 - ID3D11ShaderReflectionType.IsEqual
---

# ID3D11ShaderReflectionType::IsEqual


## -description

Indicates whether two <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a> pointers have the same underlying type.

## -parameters

### -param pType [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if the pointers have the same underlying type; otherwise returns S_FALSE.

## -remarks

IsEqual indicates whether the sources of the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a> pointers have the same underlying type.
      For example, if two <b>ID3D11ShaderReflectionType Interface</b> pointers were retrieved from variables, IsEqual can be used to see if 
      the variables have the same type.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>