---
UID: NS:d3d9types._D3DMEMORYPRESSURE
title: "_D3DMEMORYPRESSURE"
author: windows-driver-content
description: Contains data for memory pressure reporting.
old-location: direct3d9\d3dmemorypressure.htm
old-project: direct3d9
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 35360f04-1802-b3c6-8605-0a90dc8d78f5, D3DMEMORYPRESSURE, D3DMEMORYPRESSURE structure [Direct3D 9], _D3DMEMORYPRESSURE, d3d9types/D3DMEMORYPRESSURE, direct3d9.d3dmemorypressure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DMEMORYPRESSURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DMEMORYPRESSURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DMEMORYPRESSURE structure


## -description


Contains data for memory pressure reporting.


## -struct-fields




### -field BytesEvictedFromProcess

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The number of bytes that were evicted by the process during the duration of the query.


### -field SizeOfInefficientAllocation

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.


### -field LevelOfEfficiency

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The overall efficiency of the memory allocations that were placed in nonoptimal memory. The value is expressed as a percentage. For example, 
          the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient. This number should not be considered an 
          exact measurement.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

