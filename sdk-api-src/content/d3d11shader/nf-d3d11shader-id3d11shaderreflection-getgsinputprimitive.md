---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetGSInputPrimitive
title: ID3D11ShaderReflection::GetGSInputPrimitive (d3d11shader.h)
description: Gets the geometry-shader input-primitive description. (ID3D11ShaderReflection.GetGSInputPrimitive)
helpviewer_keywords: ["186739b6-e023-0b79-ed38-b3030b56e2ed","GetGSInputPrimitive","GetGSInputPrimitive method [Direct3D 11]","GetGSInputPrimitive method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetGSInputPrimitive method","ID3D11ShaderReflection.GetGSInputPrimitive","ID3D11ShaderReflection::GetGSInputPrimitive","d3d11shader/ID3D11ShaderReflection::GetGSInputPrimitive","direct3d11.id3d11shaderreflection_getgsinputprimitive"]
old-location: direct3d11\id3d11shaderreflection_getgsinputprimitive.htm
tech.root: direct3d11
ms.assetid: df34dc7e-e6aa-442d-905e-4ae11b62a781
ms.date: 12/05/2018
ms.keywords: 186739b6-e023-0b79-ed38-b3030b56e2ed, GetGSInputPrimitive, GetGSInputPrimitive method [Direct3D 11], GetGSInputPrimitive method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetGSInputPrimitive method, ID3D11ShaderReflection.GetGSInputPrimitive, ID3D11ShaderReflection::GetGSInputPrimitive, d3d11shader/ID3D11ShaderReflection::GetGSInputPrimitive, direct3d11.id3d11shaderreflection_getgsinputprimitive
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
 - ID3D11ShaderReflection::GetGSInputPrimitive
 - d3d11shader/ID3D11ShaderReflection::GetGSInputPrimitive
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
 - ID3D11ShaderReflection.GetGSInputPrimitive
---

# ID3D11ShaderReflection::GetGSInputPrimitive


## -description

Gets the geometry-shader input-primitive description.



## -returns

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D_PRIMITIVE</a></b>

The input-primitive description.  See
            <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology">D3D_PRIMITIVE_TOPOLOGY</a>,
            <a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)">D3D11_PRIMITIVE_TOPOLOGY</a>, or
            <a href="/previous-versions/windows/desktop/legacy/bb205334(v=vs.85)">D3D10_PRIMITIVE_TOPOLOGY</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
