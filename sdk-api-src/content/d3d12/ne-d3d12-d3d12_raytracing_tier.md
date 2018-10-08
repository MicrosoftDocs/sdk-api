---
UID: NE:d3d12.D3D12_RAYTRACING_TIER
title: D3D12_RAYTRACING_TIER
author: windows-sdk-content
description: Specifies the level of raytracing support on the graphics device.
old-location: direct3d12\d3d12_raytracing_tier.htm
tech.root: direct3d12
ms.assetid: 1C97DD15-5BAD-4BDC-AE43-4B6A1350B6A0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D12_RAYTRACING_TIER, D3D12_RAYTRACING_TIER enumeration, D3D12_RAYTRACING_TIER_1_0, D3D12_RAYTRACING_TIER_NOT_SUPPORTED, d3d12/D3D12_RAYTRACING_TIER, d3d12/D3D12_RAYTRACING_TIER_1_0, d3d12/D3D12_RAYTRACING_TIER_NOT_SUPPORTED, direct3d12.d3d12_raytracing_tier
ms.prod: windows
ms.technology: windows-sdk
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
---

# D3D12_RAYTRACING_TIER enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies the level of raytracing support on the graphics device.


## -enum-fields




### -field D3D12_RAYTRACING_TIER_NOT_SUPPORTED

No support for raytracing on the device.  Attempts to create any raytracing-related object will fail and using raytracing-related APIs on command lists results in undefined behavior.


### -field D3D12_RAYTRACING_TIER_1_0

The device supports tier 1 raytracing functionality. In the current release, this tier represents all available raytracing features.


## -remarks



Call <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> to determine the supported raytracing tier for a graphics device.



