---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.GetSubType
title: ID3D11ShaderReflectionType::GetSubType (d3d11shader.h)
description: Gets the base class of a class. (ID3D11ShaderReflectionType.GetSubType)
helpviewer_keywords: ["3c36b294-f376-6406-e507-0e0357b753df","GetSubType","GetSubType method [Direct3D 11]","GetSubType method [Direct3D 11]","ID3D11ShaderReflectionType interface","ID3D11ShaderReflectionType interface [Direct3D 11]","GetSubType method","ID3D11ShaderReflectionType.GetSubType","ID3D11ShaderReflectionType::GetSubType","d3d11shader/ID3D11ShaderReflectionType::GetSubType","direct3d11.id3d11shaderreflectiontype_getsubtype"]
old-location: direct3d11\id3d11shaderreflectiontype_getsubtype.htm
tech.root: direct3d11
ms.assetid: fbeae0a6-65d4-4650-a3f9-113fc0fdc6e9
ms.date: 12/05/2018
ms.keywords: 3c36b294-f376-6406-e507-0e0357b753df, GetSubType, GetSubType method [Direct3D 11], GetSubType method [Direct3D 11],ID3D11ShaderReflectionType interface, ID3D11ShaderReflectionType interface [Direct3D 11],GetSubType method, ID3D11ShaderReflectionType.GetSubType, ID3D11ShaderReflectionType::GetSubType, d3d11shader/ID3D11ShaderReflectionType::GetSubType, direct3d11.id3d11shaderreflectiontype_getsubtype
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
 - ID3D11ShaderReflectionType::GetSubType
 - d3d11shader/ID3D11ShaderReflectionType::GetSubType
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
 - ID3D11ShaderReflectionType.GetSubType
---

# ID3D11ShaderReflectionType::GetSubType


## -description

Gets the base class of a class.



## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType</a>*</b>

Returns a pointer to a <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a> containing the base class type.  Returns <b>NULL</b> if the class does not have a base class.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>
