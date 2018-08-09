---
UID: NS:d3d10.D3D10_MAPPED_TEXTURE3D
title: D3D10_MAPPED_TEXTURE3D
author: windows-sdk-content
description: Provides access to subresource data in a 3D texture.
old-location: direct3d10\d3d10_mapped_texture3d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_mapped_texture3d.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_MAPPED_TEXTURE3D, D3D10_MAPPED_TEXTURE3D structure [Direct3D 10], d3d10/D3D10_MAPPED_TEXTURE3D, d6a9ab51-df0f-5e41-8e19-a9049f06d5ed, direct3d10.d3d10_mapped_texture3d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D10_MAPPED_TEXTURE3D
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_MAPPED_TEXTURE3D
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_MAPPED_TEXTURE3D structure


## -description


Provides access to <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> data in a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">3D texture</a>.


## -struct-fields




### -field pData

Type: <b>void*</b>

Pointer to the data.


### -field RowPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The pitch, or width, or physical size (in bytes) of one row of an uncompressed texture. Since a block-compressed texture is encoded in 4x4 blocks, the <b>RowPitch</b> for a compressed texture is the number of bytes in a block of 4x4 texels. See <a href="https://msdn.microsoft.com/add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5">virtual size vs physical size</a> for more information on block compression.


### -field DepthPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The pitch or number of bytes in all rows for a single depth.


## -remarks



This structure is used to access subresource data when calling <a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">ID3D10Texture3D::Map</a>. To access data, you must cast the <b>pData</b> pointer; see <a href="https://msdn.microsoft.com/7c56991a-9364-4e2d-b681-38d007d31fad">D3D10_MAPPED_TEXTURE2D</a> for an example.

To illustrate pitch for an uncompressed texture, assume a 3D texture with mipmap levels, as shown in the following illustration.

<img alt="Illustration of a 3D texture with mipmap levels" src="images/d3d10_resource_texture3d.png"/>

It is easiest to consider the top-level texture only, as shown in the following illustration.

<img alt="Illustration of only the top-level texture" src="images/d3d10_3d_texture_1.png"/>

And then visualize the top-level texture redrawn as a series of 2D textures, each one having a different depth value. This yields several texture planes, as shown in the following illustration.

<img alt="Illustration of top-level texture drawn as 2D texture planes" src="images/d3d10_3d_texture_conceptual.png"/>

However, the actual layout of all the elements from all the texture planes looks more like the following illustration.

<img alt="Illustration of the row pitch and depth pitch in memory" src="images/d3d10_3d_texture_memory.png"/>

Use row pitch to advance a pointer between rows within a single 2D texture plane; use depth pitch to advance a pointer between 2D texture planes.




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

