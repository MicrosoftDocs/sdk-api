---
UID: NF:d3d10shader.ID3D10ShaderReflectionType.GetMemberTypeName
title: ID3D10ShaderReflectionType::GetMemberTypeName (d3d10shader.h)
description: Get a shader-reflection-variable type. (ID3D10ShaderReflectionType.GetMemberTypeName)
helpviewer_keywords: ["89050245-f34f-0590-0296-abc016ae8b42","GetMemberTypeName","GetMemberTypeName method [Direct3D 10]","GetMemberTypeName method [Direct3D 10]","ID3D10ShaderReflectionType interface","ID3D10ShaderReflectionType interface [Direct3D 10]","GetMemberTypeName method","ID3D10ShaderReflectionType.GetMemberTypeName","ID3D10ShaderReflectionType::GetMemberTypeName","d3d10shader/ID3D10ShaderReflectionType::GetMemberTypeName","direct3d10.id3d10shaderreflectiontype_getmembertypename"]
old-location: direct3d10\id3d10shaderreflectiontype_getmembertypename.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectiontype_getmembertypename.htm
ms.date: 12/05/2018
ms.keywords: 89050245-f34f-0590-0296-abc016ae8b42, GetMemberTypeName, GetMemberTypeName method [Direct3D 10], GetMemberTypeName method [Direct3D 10],ID3D10ShaderReflectionType interface, ID3D10ShaderReflectionType interface [Direct3D 10],GetMemberTypeName method, ID3D10ShaderReflectionType.GetMemberTypeName, ID3D10ShaderReflectionType::GetMemberTypeName, d3d10shader/ID3D10ShaderReflectionType::GetMemberTypeName, direct3d10.id3d10shaderreflectiontype_getmembertypename
req.header: d3d10shader.h
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
 - ID3D10ShaderReflectionType::GetMemberTypeName
 - d3d10shader/ID3D10ShaderReflectionType::GetMemberTypeName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Shader.h
api_name:
 - ID3D10ShaderReflectionType.GetMemberTypeName
---

## -description

Retrieves a shader-reflection-variable name given the index to that member of the struct type.

## -parameters

### -param Index [in]

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

A zero-based index to a member of the struct type.

## -returns

Type: **[LPCSTR](/windows/desktop/winprog/windows-data-types)**

The member name in the form of a stringified value of the [D3D_SHADER_VARIABLE_TYPE](../d3dcommon/ne-d3dcommon-d3d_shader_variable_type.md) enumeration.

## -see-also

* [ID3D10ShaderReflectionType](./nn-d3d10shader-id3d10shaderreflectiontype.md) interface
* [D3D_SHADER_VARIABLE_TYPE](../d3dcommon/ne-d3dcommon-d3d_shader_variable_type.md) enumeration
