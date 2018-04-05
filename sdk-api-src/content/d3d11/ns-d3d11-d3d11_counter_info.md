---
UID: NS:d3d11.D3D11_COUNTER_INFO
title: D3D11_COUNTER_INFO
author: windows-driver-content
description: Information about the video card's performance counter capabilities.
old-location: direct3d11\d3d11_counter_info.htm
old-project: direct3d11
ms.assetid: 64730e19-1a9e-4494-a3aa-314fd72281e1
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D11_COUNTER_INFO, D3D11_COUNTER_INFO structure [Direct3D 11], a2dae015-a80c-d3f9-238a-93195e884579, d3d11/D3D11_COUNTER_INFO, direct3d11.d3d11_counter_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_COUNTER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_COUNTER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_COUNTER_INFO structure


## -description


Information about the video card's performance counter capabilities.


## -struct-fields




### -field LastDeviceDependentCounter

Type: <b><a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a></b>

Largest device-dependent counter ID that the device supports. If none are supported, this value will be 0. Otherwise it will be greater than or equal to D3D11_COUNTER_DEVICE_DEPENDENT_0. See <a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a>.


### -field NumSimultaneousCounters

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of counters that can be simultaneously supported.


### -field NumDetectableParallelUnits

Type: <b>UINT8</b>

Number of detectable parallel units that the counter is able to discern. Values are 1 ~ 4. Use NumDetectableParallelUnits to interpret the values of the VERTEX_PROCESSING, GEOMETRY_PROCESSING, PIXEL_PROCESSING, and OTHER_GPU_PROCESSING counters. 


## -remarks



This structure is returned by <a href="https://msdn.microsoft.com/7c8824e4-33e8-46c4-bcaf-99a68fa56033">ID3D11Device::CheckCounterInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

