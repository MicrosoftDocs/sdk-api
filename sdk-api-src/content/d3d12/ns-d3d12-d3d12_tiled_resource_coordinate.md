---
UID: NS:d3d12.D3D12_TILED_RESOURCE_COORDINATE
title: D3D12_TILED_RESOURCE_COORDINATE (d3d12.h)
description: Describes the coordinates of a tiled resource.helpviewer_keywords: ["D3D12_TILED_RESOURCE_COORDINATE","D3D12_TILED_RESOURCE_COORDINATE structure","d3d12/D3D12_TILED_RESOURCE_COORDINATE","direct3d12.d3d12_tiled_resource_coordinate"]
old-location: direct3d12\d3d12_tiled_resource_coordinate.htm
tech.root: direct3d12
ms.assetid: B7C51C7A-8500-4570-99C1-AE51D6A88529
ms.date: 12/05/2018
ms.keywords: D3D12_TILED_RESOURCE_COORDINATE, D3D12_TILED_RESOURCE_COORDINATE structure, d3d12/D3D12_TILED_RESOURCE_COORDINATE, direct3d12.d3d12_tiled_resource_coordinate
f1_keywords:
- d3d12/D3D12_TILED_RESOURCE_COORDINATE
dev_langs:
- c++
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
- D3D12_TILED_RESOURCE_COORDINATE
targetos: Windows
req.typenames: D3D12_TILED_RESOURCE_COORDINATE
req.redist: 
ms.custom: 19H1
---

# D3D12_TILED_RESOURCE_COORDINATE structure


## -description


Describes the coordinates of a tiled resource.


## -struct-fields




### -field X

The x-coordinate of the tiled resource.


### -field Y

The y-coordinate of the tiled resource.


### -field Z

The z-coordinate of the tiled resource.


### -field Subresource

The index of the subresource for the tiled resource.


## -remarks



This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">CopyTiles</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a> methods.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/cd3dx12-tiled-resource-coordinate">CD3DX12_TILED_RESOURCE_COORDINATE</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

