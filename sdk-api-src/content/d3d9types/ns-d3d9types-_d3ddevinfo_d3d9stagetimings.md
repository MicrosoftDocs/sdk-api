---
UID: NS:d3d9types._D3DDEVINFO_D3D9STAGETIMINGS
title: "_D3DDEVINFO_D3D9STAGETIMINGS"
author: windows-driver-content
description: Percent of time processing shader data.
old-location: direct3d9\d3ddevinfo_d3d9stagetimings.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_d3d9stagetimings.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 89f0bac4-cac5-c94f-8768-fa176d0b6023, D3DDEVINFO_D3D9STAGETIMINGS, D3DDEVINFO_D3D9STAGETIMINGS structure [Direct3D 9], LPD3DDEVINFO_D3D9STAGETIMINGS, LPD3DDEVINFO_D3D9STAGETIMINGS structure pointer [Direct3D 9], _D3DDEVINFO_D3D9STAGETIMINGS, d3d9types/D3DDEVINFO_D3D9STAGETIMINGS, d3d9types/LPD3DDEVINFO_D3D9STAGETIMINGS, direct3d9.d3ddevinfo_d3d9stagetimings
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
req.typenames: D3DDEVINFO_D3D9STAGETIMINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_D3D9STAGETIMINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_D3D9STAGETIMINGS structure


## -description


Percent of time processing shader data.


## -struct-fields




### -field MemoryProcessingPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time in shader spent on memory accesses.


### -field ComputationProcessingPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time processing (moving data around in registers or doing mathematical operations).


## -remarks



For best performance, a balanced load is recommended.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

