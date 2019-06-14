---
UID: NS:d3d12.D3D12_FEATURE_DATA_SHADER_MODEL
title: D3D12_FEATURE_DATA_SHADER_MODEL (d3d12.h)
author: windows-sdk-content
description: Contains the supported shader model.
old-location: direct3d12\d3d12_feature_data_shader_model.htm
tech.root: direct3d12
ms.assetid: 17978B9A-D21B-4A8A-B367-12F4ABC43A94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_SHADER_MODEL, D3D12_FEATURE_DATA_SHADER_MODEL structure, d3d12/D3D12_FEATURE_DATA_SHADER_MODEL, direct3d12.d3d12_feature_data_shader_model
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_SHADER_MODEL
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_SHADER_MODEL
req.redist: 
ms.custom: 19H1
---

# D3D12_FEATURE_DATA_SHADER_MODEL structure


## -description


Contains the supported shader model.


## -struct-fields




### -field HighestShaderModel

Specifies one member of  <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d_shader_model">D3D_SHADER_MODEL</a> that indicates the maximum supported shader model.


## -remarks



Refer to  the enumeration constant D3D12_FEATURE_SHADER_MODEL in the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.
      

When used with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">ID3D12Device::CheckFeatureSupport</a> function, before calling the function initialize the <b>HighestShaderModel</b> field to the highest shader model that your  application understands.  After the function completes successfully, the <b>HighestShaderModel</b> field contains the highest shader model that is both supported by the device and no higher than the shader model passed in.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
 

 

