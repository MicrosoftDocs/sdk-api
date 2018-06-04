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

# D3D10_COUNTER enumeration


## -description


Performance counter types.


## -enum-fields




### -field D3D10_COUNTER_GPU_IDLE

Percentage of the time that the GPU is idle.


### -field D3D10_COUNTER_VERTEX_PROCESSING

Percentage of the time that the GPU does vertex processing.


### -field D3D10_COUNTER_GEOMETRY_PROCESSING

Percentage of the time that the GPU does geometry processing.


### -field D3D10_COUNTER_PIXEL_PROCESSING

Percentage of the time that the GPU does pixel processing.


### -field D3D10_COUNTER_OTHER_GPU_PROCESSING

Percentage of the time that the GPU does other processing (not vertex, geometry, or pixel processing).


### -field D3D10_COUNTER_HOST_ADAPTER_BANDWIDTH_UTILIZATION

Percentage of bandwidth used on a host adapter. Value returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> between 0.0 and 1.0 when using this counter.


### -field D3D10_COUNTER_LOCAL_VIDMEM_BANDWIDTH_UTILIZATION

Percentage of bandwidth used by the local video memory. Value returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> between 0.0 and 1.0 when using this counter


### -field D3D10_COUNTER_VERTEX_THROUGHPUT_UTILIZATION

Percentage of throughput used for vertices. Value returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> between 0.0 and 1.0 when using this counter


### -field D3D10_COUNTER_TRIANGLE_SETUP_THROUGHPUT_UTILIZATION

Percentage of throughput used for triangle setup. Value returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> between 0.0 and 1.0 when using this counter


### -field D3D10_COUNTER_FILLRATE_THROUGHPUT_UTILIZATION

Percentage of throughput used for the fillrate. Value returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> between 0.0 and 1.0 when using this counter.


### -field D3D10_COUNTER_VS_MEMORY_LIMITED

Percentage of time that a vertex shader spends sampling resources.


### -field D3D10_COUNTER_VS_COMPUTATION_LIMITED

Percentage of time that a vertex shader spends doing computations.


### -field D3D10_COUNTER_GS_MEMORY_LIMITED

Percentage of time that a geometry shader spends sampling resources.


### -field D3D10_COUNTER_GS_COMPUTATION_LIMITED

Percentage of time that a geometry shader spends doing computations.


### -field D3D10_COUNTER_PS_MEMORY_LIMITED

Percentage of time that a pixel shader spends sampling resources.


### -field D3D10_COUNTER_PS_COMPUTATION_LIMITED

Percentage of time that a pixel shader spends doing computations.


### -field D3D10_COUNTER_POST_TRANSFORM_CACHE_HIT_RATE

Percentage of vertex data that was read from the vertex cache. For example, if 6 vertices were added to the cache and 3 of them were read from the cache, then the hit rate would be 0.5.


### -field D3D10_COUNTER_TEXTURE_CACHE_HIT_RATE

Percentage of texel data that was read from the vertex cache. For example, if 6 texels were added to the cache and 3 of them were read from the cache, then the hit rate would be 0.5.


### -field D3D10_COUNTER_DEVICE_DEPENDENT_0

Start of the device-dependent counters. See remarks.


## -remarks



In addition to these performance counters, independent hardware vendors may define their own set of performance counters for their devices. The enum values for these counters would start after D3D10_COUNTER_DEVICE_DEPENDENT_0 and would be defined by those hardware vendors.

A device can support one or more of these performance counters, but it is not required to support any of them.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

