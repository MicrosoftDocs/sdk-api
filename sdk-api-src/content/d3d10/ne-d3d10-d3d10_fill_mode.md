---
UID: NE:d3d10.D3D10_FILL_MODE
title: D3D10_FILL_MODE (d3d10.h)
description: Determines the fill mode to use when rendering triangles.
helpviewer_keywords: ["0b605351-e264-0cd0-0fe1-6a7ecaa41acd","D3D10_FILL_MODE","D3D10_FILL_MODE enumeration [Direct3D 10]","D3D10_FILL_SOLID","D3D10_FILL_WIREFRAME","d3d10/D3D10_FILL_MODE","d3d10/D3D10_FILL_SOLID","d3d10/D3D10_FILL_WIREFRAME","direct3d10.d3d10_fill_mode"]
old-location: direct3d10\d3d10_fill_mode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_fill_mode.htm
ms.date: 12/05/2018
ms.keywords: 0b605351-e264-0cd0-0fe1-6a7ecaa41acd, D3D10_FILL_MODE, D3D10_FILL_MODE enumeration [Direct3D 10], D3D10_FILL_SOLID, D3D10_FILL_WIREFRAME, d3d10/D3D10_FILL_MODE, d3d10/D3D10_FILL_SOLID, d3d10/D3D10_FILL_WIREFRAME, direct3d10.d3d10_fill_mode
f1_keywords:
- d3d10/D3D10_FILL_MODE
dev_langs:
- c++
req.header: d3d10.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D10.h
api_name:
- D3D10_FILL_MODE
targetos: Windows
req.typenames: D3D10_FILL_MODE
req.redist: 
ms.custom: 19H1
---

# D3D10_FILL_MODE enumeration


## -description


Determines the fill mode to use when rendering triangles.


## -enum-fields




### -field D3D10_FILL_WIREFRAME

Draw lines connecting the vertices. <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies">Adjacent vertices</a> are not drawn.


### -field D3D10_FILL_SOLID

Fill the triangles formed by the vertices. Adjacent vertices are not drawn.


## -remarks



This enumeration is part of a rasterizer-state object description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

