---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
title: D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS (d3d11.h)
description: Describes compute shader and raw and structured buffer support in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS","D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure [Direct3D 11]","cc86b8e7-d7f6-8b3b-2873-497eec6f351e","d3d11/D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS","direct3d11.d3d11_feature_data_d3d10_x_hardware_options"]
old-location: direct3d11\d3d11_feature_data_d3d10_x_hardware_options.htm
tech.root: direct3d11
ms.assetid: d41d1d78-21c1-4373-b579-6e051d6e8929
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure [Direct3D 11], cc86b8e7-d7f6-8b3b-2873-497eec6f351e, d3d11/D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, direct3d11.d3d11_feature_data_d3d10_x_hardware_options
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
req.typenames: D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
 - d3d11/D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
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
 - D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
---

# D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure


## -description

Describes compute shader and raw and structured buffer support in the current graphics driver.

## -struct-fields

### -field ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if compute shaders and raw and structured buffers are supported; otherwise <b>FALSE</b>.

## -remarks

Direct3D 11 devices (D3D_FEATURE_LEVEL_11_0) are required to support Compute Shader model 5.0. 
      Direct3D 10.x devices (D3D_FEATURE_LEVEL_10_0, D3D_FEATURE_LEVEL_10_1) can optionally support Compute Shader model 4.0 or 4.1.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>