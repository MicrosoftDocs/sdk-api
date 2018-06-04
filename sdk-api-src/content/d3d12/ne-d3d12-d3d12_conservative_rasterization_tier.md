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

# D3D12_CONSERVATIVE_RASTERIZATION_TIER enumeration


## -description


Identifies the tier level of conservative rasterization.


## -enum-fields




### -field D3D12_CONSERVATIVE_RASTERIZATION_TIER_NOT_SUPPORTED

Conservative rasterization is not supported.


### -field D3D12_CONSERVATIVE_RASTERIZATION_TIER_1

Tier 1 enforces a maximum 1/2 pixel uncertainty region and does not support post-snap degenerates. This is good for tiled rendering, a texture atlas, light map generation and sub-pixel shadow maps.


### -field D3D12_CONSERVATIVE_RASTERIZATION_TIER_2

 Tier 2 reduces the maximum uncertainty region to 1/256 and requires post-snap degenerates not be culled. This tier is helpful for CPU-based algorithm acceleration (such as voxelization).


### -field D3D12_CONSERVATIVE_RASTERIZATION_TIER_3

 Tier 3 maintains a maximum 1/256 uncertainty region and adds support for inner input coverage. Inner input coverage adds the new value <code>SV_InnerCoverage</code> to High Level Shading Language (HLSL). This is a 32-bit scalar integer that can be specified on input to a pixel shader, and represents the underestimated conservative rasterization information (that is, whether a pixel is guaranteed-to-be-fully covered). This tier is helpful for occlusion culling.


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/081199AD-1702-4EC8-95AD-B1148C676199">Conservative Rasterization</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/E0F033D5-8042-4C39-A35D-C8FE2A95C1D2">D3D12_CONSERVATIVE_RASTERIZATION_MODE</a>
 

 

