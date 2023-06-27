---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetMinFeatureLevel
title: ID3D11ShaderReflection::GetMinFeatureLevel (d3d11shader.h)
description: Gets the minimum feature level. (ID3D11ShaderReflection.GetMinFeatureLevel)
helpviewer_keywords: ["GetMinFeatureLevel","GetMinFeatureLevel method [Direct3D 11]","GetMinFeatureLevel method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetMinFeatureLevel method","ID3D11ShaderReflection.GetMinFeatureLevel","ID3D11ShaderReflection::GetMinFeatureLevel","b8d12499-79aa-f3e6-bdd4-5ce99f2fe7d3","d3d11shader/ID3D11ShaderReflection::GetMinFeatureLevel","direct3d11.id3d11shaderreflection_getminfeaturelevel"]
old-location: direct3d11\id3d11shaderreflection_getminfeaturelevel.htm
tech.root: direct3d11
ms.assetid: b10eb64b-18ff-4248-be6e-a9c45bce3e99
ms.date: 12/05/2018
ms.keywords: GetMinFeatureLevel, GetMinFeatureLevel method [Direct3D 11], GetMinFeatureLevel method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetMinFeatureLevel method, ID3D11ShaderReflection.GetMinFeatureLevel, ID3D11ShaderReflection::GetMinFeatureLevel, b8d12499-79aa-f3e6-bdd4-5ce99f2fe7d3, d3d11shader/ID3D11ShaderReflection::GetMinFeatureLevel, direct3d11.id3d11shaderreflection_getminfeaturelevel
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
 - ID3D11ShaderReflection::GetMinFeatureLevel
 - d3d11shader/ID3D11ShaderReflection::GetMinFeatureLevel
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
 - ID3D11ShaderReflection.GetMinFeatureLevel
---

## -description

Gets the minimum feature level.

## -parameters

### -param pLevel

Type: [out] <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

A pointer to one of the enumerated values in <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>, which represents the minimum feature level.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection Interface</a>
