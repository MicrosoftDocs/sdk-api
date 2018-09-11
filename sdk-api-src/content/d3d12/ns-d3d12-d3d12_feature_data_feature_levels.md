---
UID: NS:d3d12.D3D12_FEATURE_DATA_FEATURE_LEVELS
title: D3D12_FEATURE_DATA_FEATURE_LEVELS
author: windows-sdk-content
description: Describes info about the feature levels supported by the current graphics driver.
old-location: direct3d12\d3d12_feature_data_feature_levels.htm
tech.root: direct3d12
ms.assetid: 8C709889-0C7E-4D6D-84BD-1449BB8EA96A
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_FEATURE_DATA_FEATURE_LEVELS, D3D12_FEATURE_DATA_FEATURE_LEVELS structure, d3d12/D3D12_FEATURE_DATA_FEATURE_LEVELS, direct3d12.d3d12_feature_data_feature_levels
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
 - D3D12.h
api_name:
 - D3D12_FEATURE_DATA_FEATURE_LEVELS
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_FEATURE_LEVELS
req.redist: 
---

# D3D12_FEATURE_DATA_FEATURE_LEVELS structure


## -description


Describes info about the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> supported by the current graphics driver.
        


## -struct-fields




### -field NumFeatureLevels

The number of <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> in the array at <b>pFeatureLevelsRequested</b>.
          


### -field pFeatureLevelsRequested

A pointer to an array of <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>s that the application is requesting for the driver and hardware to evaluate.
          


### -field MaxSupportedFeatureLevel

The maximum <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> that the driver and hardware support.
          


## -remarks



See <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>
 

 

