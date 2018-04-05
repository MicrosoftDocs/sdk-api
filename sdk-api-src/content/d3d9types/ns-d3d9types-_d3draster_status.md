---
UID: NS:d3d9types._D3DRASTER_STATUS
title: "_D3DRASTER_STATUS"
author: windows-driver-content
description: Describes the raster status.
old-location: direct3d9\d3draster_status.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3draster_status.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 4a2bcd9e-c3a1-733f-cb93-6e0095d38feb, D3DRASTER_STATUS, D3DRASTER_STATUS structure [Direct3D 9], LPD3DRASTER_STATUS, LPD3DRASTER_STATUS structure pointer [Direct3D 9], _D3DRASTER_STATUS, d3d9types/D3DRASTER_STATUS, d3d9types/LPD3DRASTER_STATUS, direct3d9.d3draster_status
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
req.typenames: D3DRASTER_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DRASTER_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DRASTER_STATUS structure


## -description


Describes the raster status.


## -struct-fields




### -field InVBlank

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the raster is in the vertical blank period. <b>FALSE</b> if the raster is not in the vertical blank period. 


### -field ScanLine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

If InVBlank is <b>FALSE</b>, then this value is an integer roughly corresponding to the current scan line painted by the raster. Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.

If InVBlank is <b>TRUE</b>, then this value is set to zero and can be ignored.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn940224">GetRasterStatus</a>
 

 

