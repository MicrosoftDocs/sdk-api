---
UID: NS:d3d9types._D3DVERTEXELEMENT9
title: "_D3DVERTEXELEMENT9"
author: windows-driver-content
description: Defines the vertex data layout. Each vertex can contain one or more data types, and each data type is described by a vertex element.
old-location: direct3d9\d3dvertexelement9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvertexelement9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*LPD3DVERTEXELEMENT9, D3DVERTEXELEMENT9, D3DVERTEXELEMENT9 structure [Direct3D 9], LPD3DVERTEXELEMENT9, LPD3DVERTEXELEMENT9 structure pointer [Direct3D 9], _D3DVERTEXELEMENT9, d3d9types/D3DVERTEXELEMENT9, d3d9types/LPD3DVERTEXELEMENT9, d72fc6b5-3f39-4d82-fcd8-563c3caf93e3, direct3d9.d3dvertexelement9"
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
req.typenames: D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DVERTEXELEMENT9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DVERTEXELEMENT9 structure


## -description


Defines the vertex data layout. Each vertex can contain one or more data types, and each data type is described by a vertex element.


## -struct-fields




### -field Stream

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Stream number.


### -field Offset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Offset from the beginning of the vertex data to the data associated with the particular data type.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The data type, specified as a <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>. One of several predefined types that define the data size. Some methods have an implied type.


### -field Method

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data. For more information, see <a href="https://msdn.microsoft.com/030e04a6-4e2d-4756-80ef-e4a6a0103fd1">D3DDECLMETHOD</a>.


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders. Each usage acts to bind a vertex declaration to a vertex shader. In some cases, they have a special interpretation. For example, an element that specifies D3DDECLUSAGE_NORMAL or D3DDECLUSAGE_POSITION is used by the N-patch tessellator to set up tessellation. See <a href="https://msdn.microsoft.com/ee9b46c2-b779-480c-9b5c-6d189d2af014">D3DDECLUSAGE</a> for a list of the available semantics. D3DDECLUSAGE_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).


### -field UsageIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Modifies the usage data to allow the user to specify multiple usage types.


## -remarks



Vertex data is defined using an array of <b>D3DVERTEXELEMENT9</b> structures. Use <a href="https://msdn.microsoft.com/04cf7624-2e4a-4720-9ca0-894bf963e9f9">D3DDECL_END</a> to declare the last element in the declaration.
    
    
    




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a>
 

 

