---
UID: NE:d3d12.D3D12_RAYTRACING_TIER
title: D3D12_RAYTRACING_TIER (d3d12.h)
author: windows-sdk-content
description: Specifies the level of ray tracing support on the graphics device.
old-location: direct3d12\d3d12_raytracing_tier.htm
tech.root: direct3d12
ms.assetid: 1C97DD15-5BAD-4BDC-AE43-4B6A1350B6A0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_TIER, D3D12_RAYTRACING_TIER enumeration, D3D12_RAYTRACING_TIER_1_0, D3D12_RAYTRACING_TIER_NOT_SUPPORTED, d3d12/D3D12_RAYTRACING_TIER, d3d12/D3D12_RAYTRACING_TIER_1_0, d3d12/D3D12_RAYTRACING_TIER_NOT_SUPPORTED, direct3d12.d3d12_raytracing_tier
ms.topic: enum
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
 - D3D12_RAYTRACING_TIER
product: Windows
targetos: Windows
req.typenames: D3D12_RAYTRACING_TIER
req.redist: 
ms.custom: 19H1
---

# D3D12_RAYTRACING_TIER enumeration


## -description


Specifies the level of ray tracing support on the graphics device.


## -enum-fields




### -field D3D12_RAYTRACING_TIER_NOT_SUPPORTED

No support for ray tracing on the device.  Attempts to create any ray tracing-related object will fail, and using ray tracing-related APIs on command lists results in undefined behavior.


### -field D3D12_RAYTRACING_TIER_1_0

The device supports tier 1 ray tracing functionality. In the current release, this tier represents all available ray tracing features.


## -remarks



To determine the supported ray tracing tier for a graphics device, pass <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE_D3D12_OPTIONS5</a> to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> to retrieve a <a href="https://msdn.microsoft.com/en-us/library/Mt830391(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a> struct.



