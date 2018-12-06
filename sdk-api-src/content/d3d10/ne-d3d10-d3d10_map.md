---
UID: NE:d3d10.D3D10_MAP
title: D3D10_MAP
author: windows-sdk-content
description: Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.
old-location: direct3d10\d3d10_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_map.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 851d7498-d47c-94c7-f2ce-7635689c4642, D3D10_MAP, D3D10_MAP enumeration [Direct3D 10], D3D10_MAP_READ, D3D10_MAP_READ_WRITE, D3D10_MAP_WRITE, D3D10_MAP_WRITE_DISCARD, D3D10_MAP_WRITE_NO_OVERWRITE, d3d10/D3D10_MAP, d3d10/D3D10_MAP_READ, d3d10/D3D10_MAP_READ_WRITE, d3d10/D3D10_MAP_WRITE, d3d10/D3D10_MAP_WRITE_DISCARD, d3d10/D3D10_MAP_WRITE_NO_OVERWRITE, direct3d10.d3d10_map
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - D3D10_MAP
product: Windows
targetos: Windows
req.typenames: D3D10_MAP
req.redist: 
---

# D3D10_MAP enumeration


## -description


Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.


## -enum-fields




### -field D3D10_MAP_READ

Resource is mapped for reading. The resource must have been created with read access (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_READ</a>).


### -field D3D10_MAP_WRITE

Resource is mapped for writing. The resource must have been created with write access (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_WRITE</a>).


### -field D3D10_MAP_READ_WRITE

Resource is mapped for reading and writing. The resource must have been created with read and write access (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_READ and D3D10_CPU_ACCESS_WRITE</a>).


### -field D3D10_MAP_WRITE_DISCARD

Resource is mapped for writing; the previous contents of the resource will be undefined. The resource must have been created with write access (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_WRITE</a>).


### -field D3D10_MAP_WRITE_NO_OVERWRITE

Resource is mapped for writing; the existing contents of the resource cannot be overwritten (see Remarks). This flag is only valid on vertex and index buffers. The resource must have been created with write access (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_WRITE</a>). Cannot be used on a resource created with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_CONSTANT_BUFFER</a> flag.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/c863ef55-757d-4c0b-ba59-28d30499cf79">ID3D10Buffer::Map</a>, <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>, <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">ID3D10Texture2D::Map</a>, and <a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">ID3D10Texture3D::Map</a>.

These remarks are divided into the following topics:


<ul>
<li><a href="https://docs.microsoft.com/">Meaning of D3D10_MAP_WRITE_NO_OVERWRITE</a></li>
<li><a href="https://docs.microsoft.com/">Common Usage of D3D10_MAP_WRITE_DISCARD with D3D10_MAP_WRITE_NO_OVERWRITE</a></li>
</ul>


<h3><a id="NO_OVERWRITE_DETAILS"></a><a id="no_overwrite_details"></a>Meaning of D3D10_MAP_WRITE_NO_OVERWRITE</h3>
D3D10_MAP_WRITE_NO_OVERWRITE signifies that the application promises not to write to data that the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">Input Assembler</a> (IA) stage is using. In exchange, the GPU allows the application to write to other parts of the same buffer.  The application must ensure that it does not write over any data in use by the IA stage.

For example, consider the buffer illustrated in the following diagram. If a Draw call has been issued that uses vertices 4-6, an application that calls Map on this buffer must ensure that it does not write to the vertices that the Draw call will access during rendering.

<img alt="Diagram of vertex data in different stages of utilization" src="images/d3d10_map_nooverwrite.png"/>
However, ensuring this can be difficult, because the GPU is often many frames behind the CPU in terms of which frame it is currently processing. Keeping track of which sections of a resource are being used because of calls made 2 to 5 frames ago is difficult and error-prone. Because of this, it is recommended that applications only write to the uninitialized portions of a resource when using D3D10_MAP_WRITE_NO_OVERWRITE.

<h3><a id="DISCARD_NO_OVERWRITE_USES"></a><a id="discard_no_overwrite_uses"></a>Common Usage of D3D10_MAP_WRITE_DISCARD with D3D10_MAP_WRITE_NO_OVERWRITE</h3>
D3D10_MAP_WRITE_DISCARD and D3D10_MAP_WRITE_NO_OVERWRITE are normally used in conjunction with dynamic index/vertex buffers, although they can also be used with dynamic textures.

A common use of these two flags involves filling dynamic index/vertex buffers with geometry that can be seen from the camera's current position. The first time that data is entered into the buffer on a given frame, Map is called with D3D10_MAP_WRITE_DISCARD; doing so invalidates the previous contents of the buffer. The buffer is then filled with all available data.

Subsequent writes to the buffer within the same frame should use D3D10_MAP_WRITE_NO_OVERWRITE. This will enable the CPU to access a resource that is potentially being used by the GPU as long as the restrictions described previously are respected.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

