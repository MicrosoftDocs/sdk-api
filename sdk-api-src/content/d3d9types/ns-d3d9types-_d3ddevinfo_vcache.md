---
UID: NS:d3d9types._D3DDEVINFO_VCACHE
title: "_D3DDEVINFO_VCACHE"
author: windows-driver-content
description: Vertex cache optimization hints.
old-location: direct3d9\d3ddevinfo_vcache.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_vcache.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*LPD3DDEVINFO_VCACHE, D3DDEVINFO_VCACHE, D3DDEVINFO_VCACHE structure [Direct3D 9], LPD3DDEVINFO_VCACHE, LPD3DDEVINFO_VCACHE structure pointer [Direct3D 9], _D3DDEVINFO_VCACHE, d3d9types/D3DDEVINFO_VCACHE, d3d9types/LPD3DDEVINFO_VCACHE, direct3d9.d3ddevinfo_vcache, f80be118-6239-55ac-0e4b-d8dbf48b8b7a"
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
req.typenames: D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_VCACHE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_VCACHE structure


## -description


Vertex cache optimization hints.


## -struct-fields




### -field Pattern

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Bit pattern. Return value must be the FOURCC ('C', 'A', 'C', 'H').


### -field OptMethod

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Optimizations method. Use 0 to get the longest strips. Use 1 to optimize the vertex cache usage. 


### -field CacheSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Cache size used as a target for optimization. This is required only if OptMethod is 1. 


### -field MagicNumber

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Used by internal optimization methods to determine when to restart strips. This cannot be set or modified by a user. This is required only if OptMethod is 1. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

