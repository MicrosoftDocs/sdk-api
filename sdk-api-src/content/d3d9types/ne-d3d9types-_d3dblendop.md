---
UID: NE:d3d9types._D3DBLENDOP
title: "_D3DBLENDOP"
author: windows-driver-content
description: Defines the supported blend operations. See Remarks for definitions of terms.
old-location: direct3d9\D3DBLENDOP.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dblendop.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 20252a09-5fc5-afe4-e997-bf8122013361, D3DBLENDOP, D3DBLENDOP enumeration [Direct3D 9], D3DBLENDOP_ADD, D3DBLENDOP_FORCE_DWORD, D3DBLENDOP_MAX, D3DBLENDOP_MIN, D3DBLENDOP_REVSUBTRACT, D3DBLENDOP_SUBTRACT, LPD3DBLENDOP, LPD3DBLENDOP enumeration pointer [Direct3D 9], _D3DBLENDOP, d3d9types/D3DBLENDOP, d3d9types/D3DBLENDOP_ADD, d3d9types/D3DBLENDOP_FORCE_DWORD, d3d9types/D3DBLENDOP_MAX, d3d9types/D3DBLENDOP_MIN, d3d9types/D3DBLENDOP_REVSUBTRACT, d3d9types/D3DBLENDOP_SUBTRACT, d3d9types/LPD3DBLENDOP, direct3d9.D3DBLENDOP
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
req.typenames: D3DBLENDOP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DBLENDOP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBLENDOP enumeration


## -description


Defines the supported blend operations. See Remarks for definitions of terms.


## -enum-fields




### -field D3DBLENDOP_ADD

The result is the destination added to the source.  Result = Source + Destination


### -field D3DBLENDOP_SUBTRACT

The result is the destination subtracted from to the source.  Result = Source - Destination


### -field D3DBLENDOP_REVSUBTRACT

The result is the source subtracted from the destination.  Result = Destination - Source


### -field D3DBLENDOP_MIN

The result is the minimum of the source and destination.  Result = MIN(Source, Destination)


### -field D3DBLENDOP_MAX

The result is the maximum of the source and destination.  Result = MAX(Source, Destination)


### -field D3DBLENDOP_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Source, Destination, and Result are defined as: 

<table>
<tr>
<th>Term</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>Source</td>
<td>Input</td>
<td>Color of the source pixel before the operation.</td>
</tr>
<tr>
<td>Destination</td>
<td>Input</td>
<td>Color of the pixel in the destination buffer before the operation.</td>
</tr>
<tr>
<td>Result</td>
<td>Output</td>
<td>Returned value that is the blended color resulting from the operation.</td>
</tr>
</table>
 

This enumerated type defines values used by the following render states:

<ul>
<li>D3DRS_BLENDOP</li>
<li>D3DRS_BLENDOPALPHA</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

