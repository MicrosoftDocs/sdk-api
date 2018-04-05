---
UID: NS:d3d9types._D3DMATERIAL9
title: "_D3DMATERIAL9"
author: windows-driver-content
description: Specifies material properties.
old-location: direct3d9\d3dmaterial9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dmaterial9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 1df68ab3-1d45-6810-262c-ca9af0424100, D3DMATERIAL9, D3DMATERIAL9 structure [Direct3D 9], LPD3DMATERIAL9, LPD3DMATERIAL9 structure pointer [Direct3D 9], _D3DMATERIAL9, d3d9types/D3DMATERIAL9, d3d9types/LPD3DMATERIAL9, direct3d9.d3dmaterial9
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
req.typenames: D3DMATERIAL9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DMATERIAL9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DMATERIAL9 structure


## -description


Specifies material properties.


## -struct-fields




### -field Diffuse

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Value specifying the diffuse color of the material. See <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a>. 


### -field Ambient

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Value specifying the ambient color of the material. See <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a>. 


### -field Specular

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Value specifying the specular color of the material. See <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a>. 


### -field Emissive

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Value specifying the emissive color of the material. See <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a>. 


### -field Power

Type: <b>float</b>

Floating-point value specifying the sharpness of specular highlights. The higher the value, the sharper the highlight.


## -remarks



To turn off specular highlights, set D3DRS_SPECULARENABLE to <b>FALSE</b>, using <a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>. This is the fastest option because no specular highlights will be calculated.

For more information about using the lighting engine to calculate specular lighting, see <a href="https://msdn.microsoft.com/35da0ac3-4e68-4d37-a987-405fc15d0cbf">Specular Lighting (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/834855f6-85ff-4c68-b1e7-8418042b71aa">IDirect3DDevice9::GetMaterial</a>



<a href="https://msdn.microsoft.com/52cdcd0c-1cc9-4849-91e2-822414f7f186">IDirect3DDevice9::SetMaterial</a>
 

 

