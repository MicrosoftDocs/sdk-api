---
UID: NF:d3d12shader.ID3D12ShaderReflectionType.GetSubType
title: ID3D12ShaderReflectionType::GetSubType (d3d12shader.h)
description: Gets the base class of a class. (ID3D12ShaderReflectionType.GetSubType)
helpviewer_keywords: ["GetSubType","GetSubType method","GetSubType method","ID3D12ShaderReflectionType interface","ID3D12ShaderReflectionType interface","GetSubType method","ID3D12ShaderReflectionType.GetSubType","ID3D12ShaderReflectionType::GetSubType","d3d12shader/ID3D12ShaderReflectionType::GetSubType","direct3d12.id3d12shaderreflectiontype_getsubtype"]
old-location: direct3d12\id3d12shaderreflectiontype_getsubtype.htm
tech.root: direct3d12
ms.assetid: FE91228D-F9DD-47F1-84E7-08D3C7E424C4
ms.date: 12/05/2018
ms.keywords: GetSubType, GetSubType method, GetSubType method,ID3D12ShaderReflectionType interface, ID3D12ShaderReflectionType interface,GetSubType method, ID3D12ShaderReflectionType.GetSubType, ID3D12ShaderReflectionType::GetSubType, d3d12shader/ID3D12ShaderReflectionType::GetSubType, direct3d12.id3d12shaderreflectiontype_getsubtype
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
 - ID3D12ShaderReflectionType::GetSubType
 - d3d12shader/ID3D12ShaderReflectionType::GetSubType
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
 - ID3D12ShaderReflectionType.GetSubType
---

# ID3D12ShaderReflectionType::GetSubType


## -description

Gets the base class of a class.



## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype">ID3D12ShaderReflectionType</a>*</b>

Returns a pointer to an <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype">ID3D12ShaderReflectionType</a> containing the base class type.
            Returns <b>NULL</b> if the class does not have a base class.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype">ID3D12ShaderReflectionType</a>
