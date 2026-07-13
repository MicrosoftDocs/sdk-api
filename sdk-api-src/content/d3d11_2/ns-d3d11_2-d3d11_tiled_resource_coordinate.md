---
UID: NS:d3d11_2.D3D11_TILED_RESOURCE_COORDINATE
title: D3D11_TILED_RESOURCE_COORDINATE (d3d11_2.h)
description: Describes the coordinates of a tiled resource. (D3D11_TILED_RESOURCE_COORDINATE)
helpviewer_keywords: ["D3D11_TILED_RESOURCE_COORDINATE","D3D11_TILED_RESOURCE_COORDINATE structure [Direct3D 11]","d3d11_2/D3D11_TILED_RESOURCE_COORDINATE","direct3d11.d3d11_tiled_resource_coordinate"]
old-location: direct3d11\d3d11_tiled_resource_coordinate.htm
tech.root: direct3d11
ms.assetid: 4639E5FA-44D7-4F6E-8843-17EE862BD9C4
ms.date: 12/05/2018
ms.keywords: D3D11_TILED_RESOURCE_COORDINATE, D3D11_TILED_RESOURCE_COORDINATE structure [Direct3D 11], d3d11_2/D3D11_TILED_RESOURCE_COORDINATE, direct3d11.d3d11_tiled_resource_coordinate
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: D3D11_TILED_RESOURCE_COORDINATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILED_RESOURCE_COORDINATE
 - d3d11_2/D3D11_TILED_RESOURCE_COORDINATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_2.h
api_name:
 - D3D11_TILED_RESOURCE_COORDINATE
---

# D3D11_TILED_RESOURCE_COORDINATE structure


## -description

Describes the coordinates of a tiled resource.

## -struct-fields

### -field X

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The x position of a tiled resource. Used for buffer and 1D, 2D, and 3D textures.

### -field Y

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The y position of a tiled resource. Used for 2D and 3D textures.

### -field Z

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The z position of a tiled resource. Used for 3D textures.

### -field Subresource

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A subresource index value into mipmaps and arrays. Used for 1D, 2D, and 3D textures. 

For mipmaps that use nonstandard tiling, or are packed, or both use nonstandard tiling and are packed, any subresource value that indicates any of the packed mipmaps all refer to the same tile.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
