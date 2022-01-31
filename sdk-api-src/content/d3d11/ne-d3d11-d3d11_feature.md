---
UID: NE:d3d11.D3D11_FEATURE
title: D3D11_FEATURE (d3d11.h)
description: Direct3D 11 feature options.
helpviewer_keywords: ["D3D11_FEATURE","D3D11_FEATURE enumeration [Direct3D 11]","D3D11_FEATURE_ARCHITECTURE_INFO","D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS","D3D11_FEATURE_D3D11_OPTIONS","D3D11_FEATURE_D3D11_OPTIONS1","D3D11_FEATURE_D3D11_OPTIONS2","D3D11_FEATURE_D3D11_OPTIONS3","D3D11_FEATURE_D3D11_OPTIONS4","D3D11_FEATURE_D3D9_OPTIONS","D3D11_FEATURE_D3D9_OPTIONS1","D3D11_FEATURE_D3D9_SHADOW_SUPPORT","D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT","D3D11_FEATURE_DOUBLES","D3D11_FEATURE_FORMAT_SUPPORT","D3D11_FEATURE_FORMAT_SUPPORT2","D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT","D3D11_FEATURE_MARKER_SUPPORT","D3D11_FEATURE_SHADER_CACHE","D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT","D3D11_FEATURE_THREADING","d3d11/D3D11_FEATURE","d3d11/D3D11_FEATURE_ARCHITECTURE_INFO","d3d11/D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS","d3d11/D3D11_FEATURE_D3D11_OPTIONS","d3d11/D3D11_FEATURE_D3D11_OPTIONS1","d3d11/D3D11_FEATURE_D3D11_OPTIONS2","d3d11/D3D11_FEATURE_D3D11_OPTIONS3","d3d11/D3D11_FEATURE_D3D11_OPTIONS4","d3d11/D3D11_FEATURE_D3D9_OPTIONS","d3d11/D3D11_FEATURE_D3D9_OPTIONS1","d3d11/D3D11_FEATURE_D3D9_SHADOW_SUPPORT","d3d11/D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT","d3d11/D3D11_FEATURE_DOUBLES","d3d11/D3D11_FEATURE_FORMAT_SUPPORT","d3d11/D3D11_FEATURE_FORMAT_SUPPORT2","d3d11/D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT","d3d11/D3D11_FEATURE_MARKER_SUPPORT","d3d11/D3D11_FEATURE_SHADER_CACHE","d3d11/D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT","d3d11/D3D11_FEATURE_THREADING","direct3d11.d3d11_feature","f0675a94-9721-1d35-a01a-535e5c64006d"]
old-location: direct3d11\d3d11_feature.htm
tech.root: direct3d11
ms.assetid: 48c3bf65-f077-45e6-a306-03d5760eeccb
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE, D3D11_FEATURE enumeration [Direct3D 11], D3D11_FEATURE_ARCHITECTURE_INFO, D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS, D3D11_FEATURE_D3D11_OPTIONS, D3D11_FEATURE_D3D11_OPTIONS1, D3D11_FEATURE_D3D11_OPTIONS2, D3D11_FEATURE_D3D11_OPTIONS3, D3D11_FEATURE_D3D11_OPTIONS4, D3D11_FEATURE_D3D9_OPTIONS, D3D11_FEATURE_D3D9_OPTIONS1, D3D11_FEATURE_D3D9_SHADOW_SUPPORT, D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT, D3D11_FEATURE_DOUBLES, D3D11_FEATURE_FORMAT_SUPPORT, D3D11_FEATURE_FORMAT_SUPPORT2, D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D11_FEATURE_MARKER_SUPPORT, D3D11_FEATURE_SHADER_CACHE, D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT, D3D11_FEATURE_THREADING, d3d11/D3D11_FEATURE, d3d11/D3D11_FEATURE_ARCHITECTURE_INFO, d3d11/D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS, d3d11/D3D11_FEATURE_D3D11_OPTIONS, d3d11/D3D11_FEATURE_D3D11_OPTIONS1, d3d11/D3D11_FEATURE_D3D11_OPTIONS2, d3d11/D3D11_FEATURE_D3D11_OPTIONS3, d3d11/D3D11_FEATURE_D3D11_OPTIONS4, d3d11/D3D11_FEATURE_D3D9_OPTIONS, d3d11/D3D11_FEATURE_D3D9_OPTIONS1, d3d11/D3D11_FEATURE_D3D9_SHADOW_SUPPORT, d3d11/D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT, d3d11/D3D11_FEATURE_DOUBLES, d3d11/D3D11_FEATURE_FORMAT_SUPPORT, d3d11/D3D11_FEATURE_FORMAT_SUPPORT2, d3d11/D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, d3d11/D3D11_FEATURE_MARKER_SUPPORT, d3d11/D3D11_FEATURE_SHADER_CACHE, d3d11/D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT, d3d11/D3D11_FEATURE_THREADING, direct3d11.d3d11_feature, f0675a94-9721-1d35-a01a-535e5c64006d
req.header: d3d11.h
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
req.typenames: D3D11_FEATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE
 - d3d11/D3D11_FEATURE
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
 - D3D11_FEATURE
---

## -description

Direct3D 11 feature options.

## -enum-fields

### -field D3D11_FEATURE_THREADING:0

The driver supports <a href="/windows/win32/direct3d11/overviews-direct3d-11-render-multi-thread-intro">multithreading</a>. To see an example of testing a driver for multithread support, see <a href="/windows/win32/direct3d11/overviews-direct3d-11-render-multi-thread-support">How To: Check for Driver Support</a>. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_threading">D3D11_FEATURE_DATA_THREADING</a>.

### -field D3D11_FEATURE_DOUBLES

Supports the use of the double-precision shaders in HLSL. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_doubles">D3D11_FEATURE_DATA_DOUBLES</a>.

### -field D3D11_FEATURE_FORMAT_SUPPORT

Supports the formats in <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_format_support">D3D11_FORMAT_SUPPORT</a>. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_format_support">D3D11_FEATURE_DATA_FORMAT_SUPPORT</a>.

### -field D3D11_FEATURE_FORMAT_SUPPORT2

Supports the formats in <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_format_support2">D3D11_FORMAT_SUPPORT2</a>. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_format_support2">D3D11_FEATURE_DATA_FORMAT_SUPPORT2</a>.

### -field D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS

Supports compute shaders and raw and structured buffers. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options">D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</a>.

### -field D3D11_FEATURE_D3D11_OPTIONS

Supports Direct3D 11.1 feature options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FEATURE_ARCHITECTURE_INFO

Supports specific adapter architecture. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_architecture_info">D3D11_FEATURE_DATA_ARCHITECTURE_INFO</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FEATURE_D3D9_OPTIONS

Supports Direct3D 9 feature options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d9_options">D3D11_FEATURE_DATA_D3D9_OPTIONS</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT

Supports minimum precision of shaders. For more info about HLSL minimum precision, see <a href="/windows/win32/direct3d11/direct3d-11-1-features">using HLSL minimum precision</a>. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_min_precision_support">D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FEATURE_D3D9_SHADOW_SUPPORT

Supports Direct3D 9 shadowing feature. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support">D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FEATURE_D3D11_OPTIONS1

Supports Direct3D 11.2 feature options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options1">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT

Supports Direct3D 11.2 instancing options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support">D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FEATURE_MARKER_SUPPORT

Supports Direct3D 11.2 marker options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_marker_support">D3D11_FEATURE_DATA_MARKER_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FEATURE_D3D9_OPTIONS1

Supports Direct3D 9 feature options, which includes the Direct3D 9 shadowing feature and instancing support. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d9_options1">D3D11_FEATURE_DATA_D3D9_OPTIONS1</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FEATURE_D3D11_OPTIONS2

Supports Direct3D 11.3 conservative rasterization feature options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options2">D3D11_FEATURE_DATA_D3D11_OPTIONS2</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.3.

### -field D3D11_FEATURE_D3D11_OPTIONS3

Supports Direct3D 11.4 conservative rasterization feature options. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3">D3D11_FEATURE_DATA_D3D11_OPTIONS3</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.4.

### -field D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT

Supports GPU virtual addresses. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support">D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.

### -field D3D11_FEATURE_D3D11_OPTIONS4

Supports a single boolean for NV12 shared textures. Refer to <a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4">D3D11_FEATURE_DATA_D3D11_OPTIONS4</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.4.

### -field D3D11_FEATURE_SHADER_CACHE

Supports shader cache, described in <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache">D3D11_FEATURE_DATA_SHADER_CACHE</a>.

### -field D3D11_FEATURE_D3D11_OPTIONS5

Supports a <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier">D3D11_SHARED_RESOURCE_TIER</a> to indicate a tier for shared resource support. Refer to <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5">D3D11_FEATURE_DATA_D3D11_OPTIONS5</a>.

## -remarks

This enumeration is used when querying a driver about support for these features by calling <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a>. Each value in this enumeration has a corresponding data structure that is required to be passed to the <i>pFeatureSupportData</i> parameter of <b>ID3D11Device::CheckFeatureSupport</b>.

## -see-also

<a href="/windows/win32/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core enumerations</a>

