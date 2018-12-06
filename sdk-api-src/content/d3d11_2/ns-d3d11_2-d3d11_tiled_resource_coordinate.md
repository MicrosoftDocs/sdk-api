---
UID: NS:d3d11_2.D3D11_TILED_RESOURCE_COORDINATE
title: D3D11_TILED_RESOURCE_COORDINATE
author: windows-sdk-content
description: Describes the coordinates of a tiled resource.
old-location: direct3d11\d3d11_tiled_resource_coordinate.htm
tech.root: direct3d11
ms.assetid: 4639E5FA-44D7-4F6E-8843-17EE862BD9C4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_TILED_RESOURCE_COORDINATE, D3D11_TILED_RESOURCE_COORDINATE structure [Direct3D 11], d3d11_2/D3D11_TILED_RESOURCE_COORDINATE, direct3d11.d3d11_tiled_resource_coordinate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_2.h
api_name:
 - D3D11_TILED_RESOURCE_COORDINATE
product: Windows
targetos: Windows
req.typenames: D3D11_TILED_RESOURCE_COORDINATE
req.redist: 
---

# D3D11_TILED_RESOURCE_COORDINATE structure


## -description


Describes the coordinates of a tiled resource.


## -struct-fields




### -field X

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The x position of a tiled resource. Used for buffer and 1D, 2D, and 3D textures.


### -field Y

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The y position of a tiled resource. Used for 2D and 3D textures.


### -field Z

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The z position of a tiled resource. Used for 3D textures.


### -field Subresource

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A subresource index value into mipmaps and arrays. Used for 1D, 2D, and 3D textures. 

For mipmaps that use nonstandard tiling, or are packed, or both use nonstandard tiling and are packed, any subresource value that indicates any of the packed mipmaps all refer to the same tile.


## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

