---
UID: NE:d3d9types._D3DDECLUSAGE
title: "_D3DDECLUSAGE"
author: windows-driver-content
description: Identifies the intended use of vertex data.
old-location: direct3d9\D3DDECLUSAGE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddeclusage.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 787dc122-60a6-c39d-d5eb-094372c73791, D3DDECLUSAGE, D3DDECLUSAGE enumeration [Direct3D 9], D3DDECLUSAGE_BINORMAL, D3DDECLUSAGE_BLENDINDICES, D3DDECLUSAGE_BLENDWEIGHT, D3DDECLUSAGE_COLOR, D3DDECLUSAGE_DEPTH, D3DDECLUSAGE_FOG, D3DDECLUSAGE_NORMAL, D3DDECLUSAGE_POSITION, D3DDECLUSAGE_POSITIONT, D3DDECLUSAGE_PSIZE, D3DDECLUSAGE_SAMPLE, D3DDECLUSAGE_TANGENT, D3DDECLUSAGE_TESSFACTOR, D3DDECLUSAGE_TEXCOORD, LPD3DDECLUSAGE, LPD3DDECLUSAGE enumeration pointer [Direct3D 9], _D3DDECLUSAGE, d3d9types/D3DDECLUSAGE, d3d9types/D3DDECLUSAGE_BINORMAL, d3d9types/D3DDECLUSAGE_BLENDINDICES, d3d9types/D3DDECLUSAGE_BLENDWEIGHT, d3d9types/D3DDECLUSAGE_COLOR, d3d9types/D3DDECLUSAGE_DEPTH, d3d9types/D3DDECLUSAGE_FOG, d3d9types/D3DDECLUSAGE_NORMAL, d3d9types/D3DDECLUSAGE_POSITION, d3d9types/D3DDECLUSAGE_POSITIONT, d3d9types/D3DDECLUSAGE_PSIZE, d3d9types/D3DDECLUSAGE_SAMPLE, d3d9types/D3DDECLUSAGE_TANGENT, d3d9types/D3DDECLUSAGE_TESSFACTOR, d3d9types/D3DDECLUSAGE_TEXCOORD, d3d9types/LPD3DDECLUSAGE, direct3d9.D3DDECLUSAGE
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
req.typenames: D3DDECLUSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDECLUSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDECLUSAGE enumeration


## -description


Identifies the intended use of vertex data.


## -enum-fields




### -field D3DDECLUSAGE_POSITION

Position data ranging from (-1,-1) to (1,1). Use D3DDECLUSAGE_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator. Use D3DDECLUSAGE_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening. 


### -field D3DDECLUSAGE_BLENDWEIGHT

Blending weight data. Use D3DDECLUSAGE_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.


### -field D3DDECLUSAGE_BLENDINDICES

Blending indices data. Use D3DDECLUSAGE_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.


### -field D3DDECLUSAGE_NORMAL

Vertex normal data. Use D3DDECLUSAGE_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator. Use D3DDECLUSAGE_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.


### -field D3DDECLUSAGE_PSIZE

Point size data. Use D3DDECLUSAGE_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.


### -field D3DDECLUSAGE_TEXCOORD

Texture coordinate data. Use D3DDECLUSAGE_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps_3_0. These can be used to pass user defined data. 


### -field D3DDECLUSAGE_TANGENT

Vertex tangent data.


### -field D3DDECLUSAGE_BINORMAL

Vertex binormal data. 


### -field D3DDECLUSAGE_TESSFACTOR

Single positive floating point value. Use D3DDECLUSAGE_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation. For more information about the data type, see D3DDECLTYPE_FLOAT1.


### -field D3DDECLUSAGE_POSITIONT

Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height). Use D3DDECLUSAGE_POSITIONT with a usage index of 0 to specify transformed position. When a declaration containing this is set, the pipeline does not perform vertex processing.


### -field D3DDECLUSAGE_COLOR

Vertex data contains diffuse or specular color. Use D3DDECLUSAGE_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps_3_0. Use D3DDECLUSAGE_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps_3_0.


### -field D3DDECLUSAGE_FOG

Vertex data contains fog data. Use D3DDECLUSAGE_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes. This applies to pixel shaders prior to version ps_3_0. 


### -field D3DDECLUSAGE_DEPTH

Vertex data contains depth data.


### -field D3DDECLUSAGE_SAMPLE

Vertex data contains sampler data. Use D3DDECLUSAGE_SAMPLE with a usage index of 0 to specify the displacement value to look up. It can be used only with D3DDECLUSAGE_LOOKUPPRESAMPLED or D3DDECLUSAGE_LOOKUP. 


## -remarks



Vertex data is declared with an array of <a href="https://msdn.microsoft.com/6f3c40a0-b28e-48d6-acad-ef80a919c5d7">D3DVERTEXELEMENT9</a> structures. Each element in the array contains a usage type.

For more information about vertex declarations, see <a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a>
 

 

