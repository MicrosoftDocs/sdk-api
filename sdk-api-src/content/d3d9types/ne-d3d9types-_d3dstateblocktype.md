---
UID: NE:d3d9types._D3DSTATEBLOCKTYPE
title: "_D3DSTATEBLOCKTYPE"
author: windows-driver-content
description: Predefined sets of pipeline state used by state blocks (see State Blocks Save and Restore State (Direct3D 9)).
old-location: direct3d9\D3DSTATEBLOCKTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dstateblocktype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 6cbd2f29-460e-72db-7814-f42844084aa0, D3DSBT_ALL, D3DSBT_FORCE_DWORD, D3DSBT_PIXELSTATE, D3DSBT_VERTEXSTATE, D3DSTATEBLOCKTYPE, D3DSTATEBLOCKTYPE enumeration [Direct3D 9], _D3DSTATEBLOCKTYPE, d3d9types/D3DSBT_ALL, d3d9types/D3DSBT_FORCE_DWORD, d3d9types/D3DSBT_PIXELSTATE, d3d9types/D3DSBT_VERTEXSTATE, d3d9types/D3DSTATEBLOCKTYPE, direct3d9.D3DSTATEBLOCKTYPE
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
req.typenames: D3DSTATEBLOCKTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSTATEBLOCKTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSTATEBLOCKTYPE enumeration


## -description


Predefined sets of pipeline state used by state blocks (see <a href="https://msdn.microsoft.com/6b1917a8-8685-40c3-983d-6bd2fed95642">State Blocks Save and Restore State (Direct3D 9)</a>).


## -enum-fields




### -field D3DSBT_ALL

Capture the current <a href="https://msdn.microsoft.com/e14077e4-1453-4aa3-b2de-4d3a829a819a">device state</a>.


### -field D3DSBT_PIXELSTATE

Capture the current <a href="https://msdn.microsoft.com/30624c0a-e30f-4383-bc0c-b43f42403e72">pixel state</a>.


### -field D3DSBT_VERTEXSTATE

Capture the current <a href="https://msdn.microsoft.com/cb898228-dc45-4a2a-a82e-8d64523e9b85">vertex state</a>.


### -field D3DSBT_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. Do not use this value. 


## -remarks



As the following diagram shows, vertex and pixel state are both subsets of device state.

<img alt="Diagram of device state, with vertex state and pixel state as subsets" src="images/StateSets.png"/>

There are only a few states that are considered both vertex and pixel state. These states are:

<ul>
<li>Render state: D3DRS_FOGDENSITY</li>
<li>Render state: D3DRS_FOGSTART</li>
<li>Render state: D3DRS_FOGEND</li>
<li>Texture state: D3DTSS_TEXCOORDINDEX</li>
<li>Texture state: D3DTSS_TEXTURETRANSFORMFLAGS</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<b>IDirect3DDevice9::CreateStateBlock</b>
 

 

