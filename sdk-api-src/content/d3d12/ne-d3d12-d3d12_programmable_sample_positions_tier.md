---
UID: NE:d3d12.D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER
title: D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER (d3d12.h)
author: windows-sdk-content
description: Specifies the level of support for programmable sample positions that's offered by the adapter.
old-location: direct3d12\d3d12_programmable_sample_positions_tier.htm
tech.root: direct3d12
ms.assetid: A20B501F-4F76-4CEA-AAEE-7F732E64F8F6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER, D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER enumeration, D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_1, D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_2, D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_NOT_SUPPORTED, d3d12/D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER, d3d12/D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_1, d3d12/D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_2, d3d12/D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_NOT_SUPPORTED, direct3d12.d3d12_programmable_sample_positions_tier
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
 - D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER
product: Windows
targetos: Windows
req.typenames: D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER
req.redist: 
ms.custom: 19H1
---

# D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER enumeration


## -description


Specifies the level of support for programmable sample positions that's offered by the adapter.


## -enum-fields




### -field D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_NOT_SUPPORTED

Indicates that there's no support for programmable sample positions.


### -field D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_1

Indicates that there's tier 1 support for programmable sample positions. In tier 1, a single sample pattern can be specified to repeat for every pixel (<a href="direct3d12.id3d12graphicscommandlist1_setsampleposition">SetSamplePosition</a> parameter <i>NumPixels</i> = 1) and ResolveSubResource is supported.


### -field D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER_2

Indicates that there's tier 2 support for programmable sample positions. In tier 2, four separate sample patterns can be specified for each pixel in a 2x2 grid (<a href="direct3d12.id3d12graphicscommandlist1_setsampleposition">SetSamplePosition</a> parameter <i>NumPixels</i> = 1) that repeats over the render-target or viewport, aligned on even coordinates .


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/E45DA471-E0A9-47BF-8AE5-4B8BA4B38337">D3D12_FEATURE_D3D12_DATA_OPTIONS2</a> structure to indicate the level of support offered for programmable sample positions.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

