---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetGSInputPrimitive
title: ID3D10ShaderReflection1::GetGSInputPrimitive (d3d10_1shader.h)
description: Gets the geometry-shader input-primitive description. (ID3D10ShaderReflection1.GetGSInputPrimitive)
helpviewer_keywords: ["GetGSInputPrimitive","GetGSInputPrimitive method [Direct3D 10]","GetGSInputPrimitive method [Direct3D 10]","ID3D10ShaderReflection1 interface","ID3D10ShaderReflection1 interface [Direct3D 10]","GetGSInputPrimitive method","ID3D10ShaderReflection1.GetGSInputPrimitive","ID3D10ShaderReflection1::GetGSInputPrimitive","d3d10_1shader/ID3D10ShaderReflection1::GetGSInputPrimitive","direct3d10.id3d10shaderreflection1_getgsinputprimitive","e6a690aa-8956-bd7e-467e-da156afe0b07"]
old-location: direct3d10\id3d10shaderreflection1_getgsinputprimitive.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getgsinputprimitive.htm
ms.date: 12/05/2018
ms.keywords: GetGSInputPrimitive, GetGSInputPrimitive method [Direct3D 10], GetGSInputPrimitive method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetGSInputPrimitive method, ID3D10ShaderReflection1.GetGSInputPrimitive, ID3D10ShaderReflection1::GetGSInputPrimitive, d3d10_1shader/ID3D10ShaderReflection1::GetGSInputPrimitive, direct3d10.id3d10shaderreflection1_getgsinputprimitive, e6a690aa-8956-bd7e-467e-da156afe0b07
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
 - ID3D10ShaderReflection1::GetGSInputPrimitive
 - d3d10_1shader/ID3D10ShaderReflection1::GetGSInputPrimitive
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
 - ID3D10ShaderReflection1.GetGSInputPrimitive
---

# ID3D10ShaderReflection1::GetGSInputPrimitive


## -description

Gets the geometry-shader input-primitive description.

## -parameters

### -param pPrim [in]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D10_PRIMITIVE</a>*</b>

A pointer to the input-primitive type (see <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D10_PRIMITIVE</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>
