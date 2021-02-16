---
UID: NF:d3d12shader.ID3D12ShaderReflectionType.GetMemberTypeName
title: ID3D12ShaderReflectionType::GetMemberTypeName (d3d12shader.h)
description: Gets a shader-reflection-variable type.
helpviewer_keywords: ["GetMemberTypeName","GetMemberTypeName method","GetMemberTypeName method","ID3D12ShaderReflectionType interface","ID3D12ShaderReflectionType interface","GetMemberTypeName method","ID3D12ShaderReflectionType.GetMemberTypeName","ID3D12ShaderReflectionType::GetMemberTypeName","d3d12shader/ID3D12ShaderReflectionType::GetMemberTypeName","direct3d12.id3d12shaderreflectiontype_getmembertypename"]
old-location: direct3d12\id3d12shaderreflectiontype_getmembertypename.htm
tech.root: direct3d12
ms.assetid: 113510A0-6F0D-4B30-8C6A-D0266570160E
ms.date: 12/05/2018
ms.keywords: GetMemberTypeName, GetMemberTypeName method, GetMemberTypeName method,ID3D12ShaderReflectionType interface, ID3D12ShaderReflectionType interface,GetMemberTypeName method, ID3D12ShaderReflectionType.GetMemberTypeName, ID3D12ShaderReflectionType::GetMemberTypeName, d3d12shader/ID3D12ShaderReflectionType::GetMemberTypeName, direct3d12.id3d12shaderreflectiontype_getmembertypename
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
 - ID3D12ShaderReflectionType::GetMemberTypeName
 - d3d12shader/ID3D12ShaderReflectionType::GetMemberTypeName
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
 - ID3D12ShaderReflectionType.GetMemberTypeName
---

# ID3D12ShaderReflectionType::GetMemberTypeName


## -description

Gets a shader-reflection-variable type.

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

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype">ID3D12ShaderReflectionType</a>