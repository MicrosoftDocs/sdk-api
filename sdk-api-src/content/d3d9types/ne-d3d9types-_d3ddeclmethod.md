---
UID: NE:d3d9types._D3DDECLMETHOD
title: "_D3DDECLMETHOD"
author: windows-driver-content
description: Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).
old-location: direct3d9\D3DDECLMETHOD.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddeclmethod.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDECLMETHOD, D3DDECLMETHOD enumeration [Direct3D 9], D3DDECLMETHOD_CROSSUV, D3DDECLMETHOD_DEFAULT, D3DDECLMETHOD_LOOKUP, D3DDECLMETHOD_LOOKUPPRESAMPLED, D3DDECLMETHOD_PARTIALU, D3DDECLMETHOD_PARTIALV, D3DDECLMETHOD_UV, LPD3DDECLMETHOD, LPD3DDECLMETHOD enumeration pointer [Direct3D 9], _D3DDECLMETHOD, ccc82d77-bbc5-56f9-73bd-1ad4519e2f2d, d3d9types/D3DDECLMETHOD, d3d9types/D3DDECLMETHOD_CROSSUV, d3d9types/D3DDECLMETHOD_DEFAULT, d3d9types/D3DDECLMETHOD_LOOKUP, d3d9types/D3DDECLMETHOD_LOOKUPPRESAMPLED, d3d9types/D3DDECLMETHOD_PARTIALU, d3d9types/D3DDECLMETHOD_PARTIALV, d3d9types/D3DDECLMETHOD_UV, d3d9types/LPD3DDECLMETHOD, direct3d9.D3DDECLMETHOD
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
req.typenames: D3DDECLMETHOD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDECLMETHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDECLMETHOD enumeration


## -description


Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).


## -enum-fields




### -field D3DDECLMETHOD_DEFAULT

Default value. The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations. When the tessellator is used, this element is interpolated. Otherwise vertex data is copied into the input register. The input and output type can be any value, but are always the same type.


### -field D3DDECLMETHOD_PARTIALU

Computes the tangent at a point on the rectangle or triangle patch in the U direction. The input type can be one of the following:


<ul>
<li>D3DDECLTYPE_D3DCOLOR</li>
<li>D3DDECLTYPE_FLOAT3</li>
<li>D3DDECLTYPE_FLOAT4</li>
<li>D3DDECLTYPE_SHORT4</li>
<li>D3DDECLTYPE_UBYTE4</li>
</ul>
 The output type is always D3DDECLTYPE_FLOAT3.


### -field D3DDECLMETHOD_PARTIALV

Computes the tangent at a point on the rectangle or triangle patch in the V direction. The input type can be one of the following:


<ul>
<li>D3DDECLTYPE_D3DCOLOR</li>
<li>D3DDECLTYPE_FLOAT3</li>
<li>D3DDECLTYPE_FLOAT4</li>
<li>D3DDECLTYPE_SHORT4</li>
<li>D3DDECLTYPE_UBYTE4</li>
</ul>
 The output type is always D3DDECLTYPE_FLOAT3. 


### -field D3DDECLMETHOD_CROSSUV

Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents. The input type can be one of the following:


<ul>
<li>D3DDECLTYPE_D3DCOLOR</li>
<li>D3DDECLTYPE_FLOAT3</li>
<li>D3DDECLTYPE_FLOAT4</li>
<li>D3DDECLTYPE_SHORT4</li>
<li>D3DDECLTYPE_UBYTE4</li>
</ul>
 The output type is always D3DDECLTYPE_FLOAT3.


### -field D3DDECLMETHOD_UV

Copy out the U, V values at a point on the rectangle or triangle patch. This results in a 2D float. The input type must be set to D3DDECLTYPE_UNUSED. The output data type is always D3DDECLTYPE_FLOAT2. The input stream and offset are also unused (but must be set to 0).


### -field D3DDECLMETHOD_LOOKUP

Look up a displacement map. The input type can be one of the following:


<ul>
<li>D3DDECLTYPE_FLOAT2</li>
<li>D3DDECLTYPE_FLOAT3</li>
<li>D3DDECLTYPE_FLOAT4</li>
</ul>
 Only the .x and .y components are used for the texture map lookup. The output type is always D3DDECLTYPE_FLOAT1. The device must support displacement mapping. For more information about displacement mapping, see <a href="https://msdn.microsoft.com/d6f16ff2-5a66-48a3-82c4-523faaafa6ae">Displacement Mapping (Direct3D 9)</a>. This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled. 


### -field D3DDECLMETHOD_LOOKUPPRESAMPLED

Look up a presampled displacement map. The input type must be set to D3DDECLTYPE_UNUSED; the stream index and the stream offset must be set to 0. The output type for this operation is always D3DDECLTYPE_FLOAT1. The device must support displacement mapping. For more information about displacement mapping, see <a href="https://msdn.microsoft.com/d6f16ff2-5a66-48a3-82c4-523faaafa6ae">Displacement Mapping (Direct3D 9)</a>. This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled. This method can be used only with D3DDECLUSAGE_SAMPLE.


## -remarks



The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation. Mesh data should use the default value. Patches can use any of the other implemented types.
    


Vertex data is declared with an array of <a href="https://msdn.microsoft.com/6f3c40a0-b28e-48d6-acad-ef80a919c5d7">D3DVERTEXELEMENT9</a> structures. Each element in the array contains a vertex declaration method.

In addition to using D3DDECLMETHOD_DEFAULT, a normal mesh can use D3DDECLMETHOD_LOOKUP and D3DDECLMETHOD_LOOKUPPRESAMPLED methods when N-patches are enabled.
    





## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

