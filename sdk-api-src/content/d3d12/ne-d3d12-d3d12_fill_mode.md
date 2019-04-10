---
UID: NE:d3d12.D3D12_FILL_MODE
title: D3D12_FILL_MODE (d3d12.h)
author: windows-sdk-content
description: Specifies the fill mode to use when rendering triangles.
old-location: direct3d12\d3d12_fill_mode.htm
tech.root: direct3d12
ms.assetid: 5B296AFC-4DAB-48CC-9253-93CACFDC60A8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_FILL_MODE, D3D12_FILL_MODE enumeration, D3D12_FILL_MODE_SOLID, D3D12_FILL_MODE_WIREFRAME, d3d12/D3D12_FILL_MODE, d3d12/D3D12_FILL_MODE_SOLID, d3d12/D3D12_FILL_MODE_WIREFRAME, direct3d12.d3d12_fill_mode
ms.topic: enum
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_FILL_MODE
product: Windows
targetos: Windows
req.typenames: D3D12_FILL_MODE
req.redist: 
---

# D3D12_FILL_MODE enumeration


## -description


Specifies the fill mode to use when rendering triangles.


## -enum-fields




### -field D3D12_FILL_MODE_WIREFRAME

Draw lines connecting the vertices. Adjacent vertices are not drawn.


### -field D3D12_FILL_MODE_SOLID

Fill the triangles formed by the vertices. Adjacent vertices are not drawn.


## -remarks



Fill mode is specified in a <a href="https://msdn.microsoft.com/52ECF841-72BE-44B7-BFB1-305B6981C1F4">D3D12_RASTERIZER_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/28AA8256-1CAF-484F-B219-0F0461BA947C">CD3DX12_RASTERIZER_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

