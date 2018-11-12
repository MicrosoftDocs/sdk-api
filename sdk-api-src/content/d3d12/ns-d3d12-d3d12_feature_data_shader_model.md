---
UID: NS:d3d12.D3D12_FEATURE_DATA_SHADER_MODEL
title: D3D12_FEATURE_DATA_SHADER_MODEL
author: windows-sdk-content
description: Contains the supported shader model.
old-location: direct3d12\d3d12_feature_data_shader_model.htm
tech.root: direct3d12
ms.assetid: 17978B9A-D21B-4A8A-B367-12F4ABC43A94
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_FEATURE_DATA_SHADER_MODEL, D3D12_FEATURE_DATA_SHADER_MODEL structure, d3d12/D3D12_FEATURE_DATA_SHADER_MODEL, direct3d12.d3d12_feature_data_shader_model
ms.prod: windows
ms.technology: windows-sdk
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
---

# D3D12_FEATURE_DATA_SHADER_MODEL structure


## -description


Contains the supported shader model.


## -struct-fields




### -field HighestShaderModel

Specifies one member of  <a href="https://msdn.microsoft.com/8C0674AF-CFDD-4511-B621-AB817A81B9BB">D3D_SHADER_MODEL</a> that indicates the maximum supported shader model.


## -remarks



Refer to  the enumeration constant D3D12_FEATURE_SHADER_MODEL in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.
      

When used with the <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> function, the <b>HighestShaderModel</b> field should be initialized before invocation to the highest shader model that the application understands. After a successful invocation, the <b>HighestShaderModel</b> field will contain the highest shader model supported by the device that is no higher than the initial value.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

