---
UID: NS:d3d11.D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT
title: D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT (d3d11.h)
description: Describes precision support options for shaders in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT","D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT","direct3d11.d3d11_feature_data_shader_min_precision_support"]
old-location: direct3d11\d3d11_feature_data_shader_min_precision_support.htm
tech.root: direct3d11
ms.assetid: 4494A896-E73E-4A41-BC73-F9BD49510276
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT, D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT, direct3d11.d3d11_feature_data_shader_min_precision_support
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT
 - d3d11/D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT
---

# D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT structure


## -description

<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes precision support  options for shaders in the current graphics driver.

## -struct-fields

### -field PixelShaderMinPrecision

A combination of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_shader_min_precision_support">D3D11_SHADER_MIN_PRECISION_SUPPORT</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies minimum precision levels that the driver supports for the pixel shader. A value of zero indicates that the driver supports only full 32-bit precision for the pixel shader.

### -field AllOtherShaderStagesMinPrecision

A combination of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_shader_min_precision_support">D3D11_SHADER_MIN_PRECISION_SUPPORT</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies minimum precision levels that the driver supports for all other shader stages. A value of zero indicates that the driver supports only full 32-bit precision for all other shader stages.

## -remarks

For hardware at Direct3D 10 and higher <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a>, the runtime sets both members identically.  For hardware at Direct3D 9.3 and lower feature levels, the runtime can set a lower precision support in the <b>PixelShaderMinPrecision</b> member than the <b>AllOtherShaderStagesMinPrecision</b> member; for 9.3 and lower, all other shader stages represent only the vertex shader.

For more info about HLSL minimum precision, see <a href="/windows/desktop/direct3d11/direct3d-11-1-features">using HLSL minimum precision</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>