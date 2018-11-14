---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS5
title: D3D12_FEATURE_DATA_D3D12_OPTIONS5
author: windows-sdk-content
description: Used to indicate the level of support that the adapter provides for optional features of Direct3D 12.
old-location: direct3d12\d3d12_feature_data_d3d12_options5.htm
tech.root: direct3d12
ms.assetid: 7B786C22-56C1-44A0-BE67-DE04EB367FD2
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS5, D3D12_FEATURE_DATA_D3D12_OPTIONS5 structure, PD3D12_FEATURE_DATA_D3D12_OPTIONS5, PD3D12_FEATURE_DATA_D3D12_OPTIONS5 structure pointer, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS5, d3d12/PD3D12_FEATURE_DATA_D3D12_OPTIONS5, direct3d12.d3d12_feature_data_d3d12_options5
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS5
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS5
req.redist: 
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS5 structure


## -description


Used to indicate the level of support that the adapter provides for optional features of Direct3D 12.


## -struct-fields




### -field SRVOnlyTiledResourceTier3

A boolean value indicating whether the options require shader-resource view tier 3 tiled resource support. For more information, see <a href="https://msdn.microsoft.com/ADBA96C3-BD9E-4F12-89C8-371F6F7D369D">D3D12_TILED_RESOURCES_TIER</a>.


### -field RenderPassesTier

The extent to which a UMD/HW efficiently supports render passes.



#### RaytracingTier

Specifies the level of raytracing support on the graphics device.


### -field RaytracingTier

 



