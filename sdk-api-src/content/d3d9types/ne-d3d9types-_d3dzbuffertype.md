---
UID: NE:d3d9types._D3DZBUFFERTYPE
title: "_D3DZBUFFERTYPE"
author: windows-driver-content
description: Defines constants that describe depth-buffer formats.
old-location: direct3d9\D3DZBUFFERTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dzbuffertype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 5ae25df6-50ef-64a0-cdb0-4235fea2d2ab, D3DZBUFFERTYPE, D3DZBUFFERTYPE enumeration [Direct3D 9], D3DZB_FALSE, D3DZB_FORCE_DWORD, D3DZB_TRUE, D3DZB_USEW, LPD3DZBUFFERTYPE, LPD3DZBUFFERTYPE enumeration pointer [Direct3D 9], _D3DZBUFFERTYPE, d3d9types/D3DZBUFFERTYPE, d3d9types/D3DZB_FALSE, d3d9types/D3DZB_FORCE_DWORD, d3d9types/D3DZB_TRUE, d3d9types/D3DZB_USEW, d3d9types/LPD3DZBUFFERTYPE, direct3d9.D3DZBUFFERTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3DZBUFFERTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DZBUFFERTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DZBUFFERTYPE enumeration


## -description


Defines constants that describe depth-buffer formats.


## -enum-fields




### -field D3DZB_FALSE

Disable depth buffering. 


### -field D3DZB_TRUE

Enable z-buffering. 


### -field D3DZB_USEW

Enable w-buffering. 


### -field D3DZB_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Members of this enumerated type are used with the D3DRS_ZENABLE render state.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

