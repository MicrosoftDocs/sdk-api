---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

