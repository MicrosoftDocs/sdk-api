---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.GetMemberTypeName
title: ID3D11ShaderReflectionType::GetMemberTypeName (d3d11shader.h)
description: Get a shader-reflection-variable type. (ID3D11ShaderReflectionType.GetMemberTypeName)
helpviewer_keywords: ["GetMemberTypeName","GetMemberTypeName method [Direct3D 11]","GetMemberTypeName method [Direct3D 11]","ID3D11ShaderReflectionType interface","ID3D11ShaderReflectionType interface [Direct3D 11]","GetMemberTypeName method","ID3D11ShaderReflectionType.GetMemberTypeName","ID3D11ShaderReflectionType::GetMemberTypeName","d3d11shader/ID3D11ShaderReflectionType::GetMemberTypeName","direct3d11.id3d11shaderreflectiontype_getmembertypename","f251ed0c-ec44-be56-47ea-1524e2323451"]
old-location: direct3d11\id3d11shaderreflectiontype_getmembertypename.htm
tech.root: direct3d11
ms.assetid: 81f26565-f85a-4740-af3f-92b760d8b72f
ms.date: 12/05/2018
ms.keywords: GetMemberTypeName, GetMemberTypeName method [Direct3D 11], GetMemberTypeName method [Direct3D 11],ID3D11ShaderReflectionType interface, ID3D11ShaderReflectionType interface [Direct3D 11],GetMemberTypeName method, ID3D11ShaderReflectionType.GetMemberTypeName, ID3D11ShaderReflectionType::GetMemberTypeName, d3d11shader/ID3D11ShaderReflectionType::GetMemberTypeName, direct3d11.id3d11shaderreflectiontype_getmembertypename, f251ed0c-ec44-be56-47ea-1524e2323451
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
 - ID3D11ShaderReflectionType::GetMemberTypeName
 - d3d11shader/ID3D11ShaderReflectionType::GetMemberTypeName
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
 - ID3D11ShaderReflectionType.GetMemberTypeName
---

# ID3D11ShaderReflectionType::GetMemberTypeName


## -description

Get a shader-reflection-variable type.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The variable type.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>
