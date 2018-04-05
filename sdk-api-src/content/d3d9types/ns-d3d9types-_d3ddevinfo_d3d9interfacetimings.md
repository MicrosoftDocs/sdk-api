---
UID: NS:d3d9types._D3DDEVINFO_D3D9INTERFACETIMINGS
title: "_D3DDEVINFO_D3D9INTERFACETIMINGS"
author: windows-driver-content
description: Percent of time processing data in the driver. These statistics may help identify cases when the driver is waiting for other resources.
old-location: direct3d9\d3ddevinfo_d3d9interfacetimings.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_d3d9interfacetimings.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDEVINFO_D3D9INTERFACETIMINGS, D3DDEVINFO_D3D9INTERFACETIMINGS structure [Direct3D 9], LPD3DDEVINFO_D3D9INTERFACETIMINGS, LPD3DDEVINFO_D3D9INTERFACETIMINGS structure pointer [Direct3D 9], _D3DDEVINFO_D3D9INTERFACETIMINGS, b7135939-2a7e-bfed-c0a6-241d56d63cc1, d3d9types/D3DDEVINFO_D3D9INTERFACETIMINGS, d3d9types/LPD3DDEVINFO_D3D9INTERFACETIMINGS, direct3d9.d3ddevinfo_d3d9interfacetimings
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
req.typenames: D3DDEVINFO_D3D9INTERFACETIMINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_D3D9INTERFACETIMINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_D3D9INTERFACETIMINGS structure


## -description


Percent of time processing data in the driver. These statistics may help identify cases when the driver is waiting for other resources.


## -struct-fields




### -field WaitingForGPUToUseApplicationResourceTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_DONOTWAIT</a>    wasn't specified).


### -field WaitingForGPUToAcceptMoreCommandsTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more. This indicates the driver has run out of room to send commands to the GPU.


### -field WaitingForGPUToStayWithinLatencyTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames. 



If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames. This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input. In general, the driver can track the number of times <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a> is called to prevent queuing up more than three frames of rendering work.


### -field WaitingForGPUExclusiveResourceTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel). An application may want to avoid using a non-pipelined resource for performance reasons.


### -field WaitingForGPUOtherTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percentage of time the driver spent waiting for other GPU processing.


## -remarks



These metrics help identify when a driver is waiting and what it is waiting for. High percentages are not necessarily a problem.

These system-global metrics may or may not be implemented. Depending on the specific hardware, these metrics may not support multiple queries simultaneously.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

