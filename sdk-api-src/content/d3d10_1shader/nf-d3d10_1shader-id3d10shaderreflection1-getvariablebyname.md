---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetVariableByName
title: ID3D10ShaderReflection1::GetVariableByName (d3d10_1shader.h)
description: Gets a variable by name. (ID3D10ShaderReflection1.GetVariableByName)
helpviewer_keywords: ["949e282a-c8c8-2ae4-0a72-0b158bbcc614","GetVariableByName","GetVariableByName method [Direct3D 10]","GetVariableByName method [Direct3D 10]","ID3D10ShaderReflection1 interface","ID3D10ShaderReflection1 interface [Direct3D 10]","GetVariableByName method","ID3D10ShaderReflection1.GetVariableByName","ID3D10ShaderReflection1::GetVariableByName","d3d10_1shader/ID3D10ShaderReflection1::GetVariableByName","direct3d10.id3d10shaderreflection1_getvariablebyname"]
old-location: direct3d10\id3d10shaderreflection1_getvariablebyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getvariablebyname.htm
ms.date: 12/05/2018
ms.keywords: 949e282a-c8c8-2ae4-0a72-0b158bbcc614, GetVariableByName, GetVariableByName method [Direct3D 10], GetVariableByName method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetVariableByName method, ID3D10ShaderReflection1.GetVariableByName, ID3D10ShaderReflection1::GetVariableByName, d3d10_1shader/ID3D10ShaderReflection1::GetVariableByName, direct3d10.id3d10shaderreflection1_getvariablebyname
req.header: d3d10_1shader.h
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
 - ID3D10ShaderReflection1::GetVariableByName
 - d3d10_1shader/ID3D10ShaderReflection1::GetVariableByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1Shader.h
api_name:
 - ID3D10ShaderReflection1.GetVariableByName
---

# ID3D10ShaderReflection1::GetVariableByName


## -description

Gets a variable by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a>*</b>

A pointer to a string containing the variable name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionvariable">ID3D10ShaderReflectionVariable</a>*</b>

Returns a <a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionvariable">ID3D10ShaderReflectionVariable Interface</a> interface.

## -remarks

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>
