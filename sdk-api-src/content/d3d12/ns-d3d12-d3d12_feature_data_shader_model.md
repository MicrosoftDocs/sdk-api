---
UID: NS:d3d12.D3D12_FEATURE_DATA_SHADER_MODEL
title: D3D12_FEATURE_DATA_SHADER_MODEL (d3d12.h)
description: Contains the supported shader model.
helpviewer_keywords: ["D3D12_FEATURE_DATA_SHADER_MODEL","D3D12_FEATURE_DATA_SHADER_MODEL structure","d3d12/D3D12_FEATURE_DATA_SHADER_MODEL","direct3d12.d3d12_feature_data_shader_model"]
old-location: direct3d12\d3d12_feature_data_shader_model.htm
tech.root: direct3d12
ms.assetid: 17978B9A-D21B-4A8A-B367-12F4ABC43A94
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_SHADER_MODEL, D3D12_FEATURE_DATA_SHADER_MODEL structure, d3d12/D3D12_FEATURE_DATA_SHADER_MODEL, direct3d12.d3d12_feature_data_shader_model
req.header: d3d12.h
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
req.typenames: D3D12_FEATURE_DATA_SHADER_MODEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_SHADER_MODEL
 - d3d12/D3D12_FEATURE_DATA_SHADER_MODEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_SHADER_MODEL
---

# D3D12_FEATURE_DATA_SHADER_MODEL structure


## -description

Contains the supported shader model.

## -struct-fields

### -field HighestShaderModel

Specifies one member of  <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_shader_model">D3D_SHADER_MODEL</a> that indicates the maximum supported shader model.

## -remarks

Refer to  the enumeration constant D3D12_FEATURE_SHADER_MODEL in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.
      

When used with the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">ID3D12Device::CheckFeatureSupport</a> function, before calling the function initialize the <b>HighestShaderModel</b> field to the highest shader model that your  application understands.  After the function completes successfully, the <b>HighestShaderModel</b> field contains the highest shader model that is both supported by the device and no higher than the shader model passed in.

Note that <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">ID3D12Device::CheckFeatureSupport</a> will return E_INVALIDARG if HighestShaderModel is not known by the current runtime. For this reason, it is recommended that this is called in a loop with decreasing shader models to determine the highest supported shader model. Alternatively, use the caps checking helper to simplify this: https://devblogs.microsoft.com/directx/introducing-a-new-api-for-checking-feature-support-in-direct3d-12.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
