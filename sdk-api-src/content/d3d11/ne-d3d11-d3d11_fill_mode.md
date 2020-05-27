---
UID: NE:d3d11.D3D11_FILL_MODE
title: D3D11_FILL_MODE (d3d11.h)
description: Determines the fill mode to use when rendering triangles.
helpviewer_keywords: ["D3D11_FILL_MODE","D3D11_FILL_MODE enumeration [Direct3D 11]","D3D11_FILL_SOLID","D3D11_FILL_WIREFRAME","d3d11/D3D11_FILL_MODE","d3d11/D3D11_FILL_SOLID","d3d11/D3D11_FILL_WIREFRAME","d7c0d124-b654-14ba-20c5-ab454511f4d2","direct3d11.d3d11_fill_mode"]
old-location: direct3d11\d3d11_fill_mode.htm
tech.root: direct3d11
ms.assetid: 853a7df5-4740-40dd-9188-2b399f3aae68
ms.date: 12/05/2018
ms.keywords: D3D11_FILL_MODE, D3D11_FILL_MODE enumeration [Direct3D 11], D3D11_FILL_SOLID, D3D11_FILL_WIREFRAME, d3d11/D3D11_FILL_MODE, d3d11/D3D11_FILL_SOLID, d3d11/D3D11_FILL_WIREFRAME, d7c0d124-b654-14ba-20c5-ab454511f4d2, direct3d11.d3d11_fill_mode
f1_keywords:
- d3d11/D3D11_FILL_MODE
dev_langs:
- c++
req.header: d3d11.h
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
- D3D11.h
api_name:
- D3D11_FILL_MODE
targetos: Windows
req.typenames: D3D11_FILL_MODE
req.redist: 
ms.custom: 19H1
---

# D3D11_FILL_MODE enumeration


## -description


Determines the fill mode to use when rendering triangles.


## -enum-fields




### -field D3D11_FILL_WIREFRAME

Draw lines connecting the vertices. Adjacent vertices are not drawn.


### -field D3D11_FILL_SOLID

Fill the triangles formed by the vertices. Adjacent vertices are not drawn.


## -remarks



This enumeration is part of a rasterizer-state object description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
 

 

