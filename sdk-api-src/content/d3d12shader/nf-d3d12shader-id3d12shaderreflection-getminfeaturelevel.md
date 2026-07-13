---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetMinFeatureLevel
title: ID3D12ShaderReflection::GetMinFeatureLevel (d3d12shader.h)
description: Gets the minimum feature level. (ID3D12ShaderReflection.GetMinFeatureLevel)
helpviewer_keywords: ["GetMinFeatureLevel","GetMinFeatureLevel method","GetMinFeatureLevel method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetMinFeatureLevel method","ID3D12ShaderReflection.GetMinFeatureLevel","ID3D12ShaderReflection::GetMinFeatureLevel","d3d12shader/ID3D12ShaderReflection::GetMinFeatureLevel","direct3d12.id3d12shaderreflection_getminfeaturelevel"]
old-location: direct3d12\id3d12shaderreflection_getminfeaturelevel.htm
tech.root: direct3d12
ms.assetid: DE1FC45B-DA2B-41B6-A732-62BA886F51C2
ms.date: 12/05/2018
ms.keywords: GetMinFeatureLevel, GetMinFeatureLevel method, GetMinFeatureLevel method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetMinFeatureLevel method, ID3D12ShaderReflection.GetMinFeatureLevel, ID3D12ShaderReflection::GetMinFeatureLevel, d3d12shader/ID3D12ShaderReflection::GetMinFeatureLevel, direct3d12.id3d12shaderreflection_getminfeaturelevel
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
 - ID3D12ShaderReflection::GetMinFeatureLevel
 - d3d12shader/ID3D12ShaderReflection::GetMinFeatureLevel
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
 - ID3D12ShaderReflection.GetMinFeatureLevel
---

# ID3D12ShaderReflection::GetMinFeatureLevel


## -description

Gets the minimum feature level.

## -parameters

### -param pLevel [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

A pointer to one of the enumerated values in <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>, which represents the minimum feature level.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>
