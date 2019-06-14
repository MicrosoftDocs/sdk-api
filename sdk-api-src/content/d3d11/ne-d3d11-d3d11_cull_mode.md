---
UID: NE:d3d11.D3D11_CULL_MODE
title: D3D11_CULL_MODE (d3d11.h)
author: windows-sdk-content
description: Indicates triangles facing a particular direction are not drawn.
old-location: direct3d11\d3d11_cull_mode.htm
tech.root: direct3d11
ms.assetid: 437c4e2f-f120-44db-b0ce-f4dd4e666814
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6a382bf1-a9ce-3b9b-41ed-46a4fee9ef85, D3D11_CULL_BACK, D3D11_CULL_FRONT, D3D11_CULL_MODE, D3D11_CULL_MODE enumeration [Direct3D 11], D3D11_CULL_NONE, d3d11/D3D11_CULL_BACK, d3d11/D3D11_CULL_FRONT, d3d11/D3D11_CULL_MODE, d3d11/D3D11_CULL_NONE, direct3d11.d3d11_cull_mode
ms.topic: enum
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
 - D3D11_CULL_MODE
product: Windows
targetos: Windows
req.typenames: D3D11_CULL_MODE
req.redist: 
ms.custom: 19H1
---

# D3D11_CULL_MODE enumeration


## -description


Indicates triangles facing a particular direction are not drawn.


## -enum-fields




### -field D3D11_CULL_NONE

Always draw all triangles.


### -field D3D11_CULL_FRONT

Do not draw triangles that are front-facing.


### -field D3D11_CULL_BACK

Do not draw triangles that are back-facing.


## -remarks



This enumeration is part of a rasterizer-state object description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
 

 

