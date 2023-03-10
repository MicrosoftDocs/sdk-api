---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.ImplementsInterface
title: ID3D11ShaderReflectionType::ImplementsInterface (d3d11shader.h)
description: Indicates whether a class type implements an interface. (ID3D11ShaderReflectionType.ImplementsInterface)
helpviewer_keywords: ["806550ed-6d2f-16a0-b48b-9510e852ab3b","ID3D11ShaderReflectionType interface [Direct3D 11]","ImplementsInterface method","ID3D11ShaderReflectionType.ImplementsInterface","ID3D11ShaderReflectionType::ImplementsInterface","ImplementsInterface","ImplementsInterface method [Direct3D 11]","ImplementsInterface method [Direct3D 11]","ID3D11ShaderReflectionType interface","d3d11shader/ID3D11ShaderReflectionType::ImplementsInterface","direct3d11.id3d11shaderreflectiontype_implementsinterface"]
old-location: direct3d11\id3d11shaderreflectiontype_implementsinterface.htm
tech.root: direct3d11
ms.assetid: 783f6026-10d1-4b24-a2d8-bbe26ae450eb
ms.date: 12/05/2018
ms.keywords: 806550ed-6d2f-16a0-b48b-9510e852ab3b, ID3D11ShaderReflectionType interface [Direct3D 11],ImplementsInterface method, ID3D11ShaderReflectionType.ImplementsInterface, ID3D11ShaderReflectionType::ImplementsInterface, ImplementsInterface, ImplementsInterface method [Direct3D 11], ImplementsInterface method [Direct3D 11],ID3D11ShaderReflectionType interface, d3d11shader/ID3D11ShaderReflectionType::ImplementsInterface, direct3d11.id3d11shaderreflectiontype_implementsinterface
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
 - ID3D11ShaderReflectionType::ImplementsInterface
 - d3d11shader/ID3D11ShaderReflectionType::ImplementsInterface
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
 - ID3D11ShaderReflectionType.ImplementsInterface
---

# ID3D11ShaderReflectionType::ImplementsInterface


## -description

Indicates whether a class type implements an interface.

## -parameters

### -param pBase [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if the interface is implemented; otherwise return S_FALSE.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectiontype">ID3D11ShaderReflectionType Interface</a>
