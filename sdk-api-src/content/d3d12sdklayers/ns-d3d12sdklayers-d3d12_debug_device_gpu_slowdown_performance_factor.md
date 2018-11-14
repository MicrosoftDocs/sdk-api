---
UID: NS:d3d12sdklayers.D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
title: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
author: windows-sdk-content
description: Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.
old-location: direct3d12\d3d12_debug_device_gpu_slowdown_performance_factor.htm
tech.root: direct3d12
ms.assetid: C137DFAA-7AB9-49A6-882D-61ADE6E9E046
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR, D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure, d3d12sdklayers/D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR, direct3d12.d3d12_debug_device_gpu_slowdown_performance_factor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
 - d3d12sdklayers.h
api_name:
 - D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
product: Windows
targetos: Windows
req.typenames: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
req.redist: 
---

# D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure


## -description


Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.


## -struct-fields




### -field SlowdownFactor

Specifies the amount of slowdown artificially applied, as a factor of the nominal time for the fence to signal. The default value is 0.


## -remarks



The SlowdownFactor is applied by artificially delaying the time it takes for a fence to signal. When SlowdownFactor is non-zero, the time taken for a fence to signal is approximately 1.0 + SlowdownFactor times the length of the nominal timing.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

