---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

