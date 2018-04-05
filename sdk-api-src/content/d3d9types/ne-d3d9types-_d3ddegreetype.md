---
UID: NE:d3d9types._D3DDEGREETYPE
title: "_D3DDEGREETYPE"
author: windows-driver-content
description: Defines the degree of the variables in the equation that describes a curve.
old-location: direct3d9\D3DDEGREETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddegreetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DCULL_FORCE_DWORD, D3DDEGREETYPE, D3DDEGREETYPE enumeration [Direct3D 9], D3DDEGREE_CUBIC, D3DDEGREE_LINEAR, D3DDEGREE_QUADRATIC, D3DDEGREE_QUINTIC, LPD3DDEGREETYPE, LPD3DDEGREETYPE enumeration pointer [Direct3D 9], _D3DDEGREETYPE, d3d9types/D3DCULL_FORCE_DWORD, d3d9types/D3DDEGREETYPE, d3d9types/D3DDEGREE_CUBIC, d3d9types/D3DDEGREE_LINEAR, d3d9types/D3DDEGREE_QUADRATIC, d3d9types/D3DDEGREE_QUINTIC, d3d9types/LPD3DDEGREETYPE, direct3d9.D3DDEGREETYPE, e988272b-c363-4a73-8731-5b5bb419b009
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
req.typenames: D3DDEGREETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEGREETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEGREETYPE enumeration


## -description


Defines the degree of the variables in the equation that describes a curve.


## -enum-fields




### -field D3DDEGREE_LINEAR

Curve is described by variables of first order.


### -field D3DDEGREE_QUADRATIC

Curve is described by variables of second order.


### -field D3DDEGREE_CUBIC

Curve is described by variables of third order.


### -field D3DDEGREE_QUINTIC

Curve is described by variables of fourth order.


### -field D3DDEGREE_FORCE_DWORD




#### - D3DCULL_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The values in this enumeration are used to describe the curves used by rectangle and triangle patches. For more information, see D3DRS_CULLMODE.




## -see-also




<a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

