---
UID: NE:d3d10.D3D10_MAP
title: D3D10_MAP (d3d10.h)
description: Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.
helpviewer_keywords: ["851d7498-d47c-94c7-f2ce-7635689c4642","D3D10_MAP","D3D10_MAP enumeration [Direct3D 10]","D3D10_MAP_READ","D3D10_MAP_READ_WRITE","D3D10_MAP_WRITE","D3D10_MAP_WRITE_DISCARD","D3D10_MAP_WRITE_NO_OVERWRITE","d3d10/D3D10_MAP","d3d10/D3D10_MAP_READ","d3d10/D3D10_MAP_READ_WRITE","d3d10/D3D10_MAP_WRITE","d3d10/D3D10_MAP_WRITE_DISCARD","d3d10/D3D10_MAP_WRITE_NO_OVERWRITE","direct3d10.d3d10_map"]
old-location: direct3d10\d3d10_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_map.htm
ms.date: 12/05/2018
ms.keywords: 851d7498-d47c-94c7-f2ce-7635689c4642, D3D10_MAP, D3D10_MAP enumeration [Direct3D 10], D3D10_MAP_READ, D3D10_MAP_READ_WRITE, D3D10_MAP_WRITE, D3D10_MAP_WRITE_DISCARD, D3D10_MAP_WRITE_NO_OVERWRITE, d3d10/D3D10_MAP, d3d10/D3D10_MAP_READ, d3d10/D3D10_MAP_READ_WRITE, d3d10/D3D10_MAP_WRITE, d3d10/D3D10_MAP_WRITE_DISCARD, d3d10/D3D10_MAP_WRITE_NO_OVERWRITE, direct3d10.d3d10_map
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
targetos: Windows
req.typenames: D3D10_MAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MAP
 - d3d10/D3D10_MAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_MAP
---

# D3D10_MAP enumeration


## -description

Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.

## -enum-fields

### -field D3D10_MAP_READ:1

Resource is mapped for reading. The resource must have been created with read access (see <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_READ</a>).

### -field D3D10_MAP_WRITE:2

Resource is mapped for writing. The resource must have been created with write access (see <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_WRITE</a>).

### -field D3D10_MAP_READ_WRITE:3

Resource is mapped for reading and writing. The resource must have been created with read and write access (see <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_READ and D3D10_CPU_ACCESS_WRITE</a>).

### -field D3D10_MAP_WRITE_DISCARD:4

Resource is mapped for writing; the previous contents of the resource will be undefined. The resource must have been created with write access (see <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_WRITE</a>).

### -field D3D10_MAP_WRITE_NO_OVERWRITE:5

Resource is mapped for writing; the existing contents of the resource cannot be overwritten (see Remarks). This flag is only valid on vertex and index buffers. The resource must have been created with write access (see <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_WRITE</a>). Cannot be used on a resource created with the <a href="/windows/win32/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_CONSTANT_BUFFER</a> flag.

## -remarks

This enumeration is used in <a href="/windows/win32/api/d3d10/nf-d3d10-id3d10buffer-map">ID3D10Buffer::Map</a>, <a href="/windows/win32/api/d3d10/nf-d3d10-id3d10texture1d-map">ID3D10Texture1D::Map</a>, <a href="/windows/win32/api/d3d10/nf-d3d10-id3d10texture2d-map">ID3D10Texture2D::Map</a>, and <a href="/windows/win32/api/d3d10/nf-d3d10-id3d10texture3d-map">ID3D10Texture3D::Map</a>.


<h3><a id="NO_OVERWRITE_DETAILS"></a><a id="no_overwrite_details"></a>Meaning of D3D10_MAP_WRITE_NO_OVERWRITE</h3>
D3D10_MAP_WRITE_NO_OVERWRITE signifies that the application promises not to write to data that the <a href="/windows/win32/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">Input Assembler</a> (IA) stage is using. In exchange, the GPU allows the application to write to other parts of the same buffer.  The application must ensure that it does not write over any data in use by the IA stage.

For example, consider the buffer illustrated in the following diagram. If a Draw call has been issued that uses vertices 4-6, an application that calls Map on this buffer must ensure that it does not write to the vertices that the Draw call will access during rendering.

<img alt="Diagram of vertex data in different stages of utilization" src="./images/d3d10_map_nooverwrite.png"/>
However, ensuring this can be difficult, because the GPU is often many frames behind the CPU in terms of which frame it is currently processing. Keeping track of which sections of a resource are being used because of calls made 2 to 5 frames ago is difficult and error-prone. Because of this, it is recommended that applications only write to the uninitialized portions of a resource when using D3D10_MAP_WRITE_NO_OVERWRITE.

<h3><a id="DISCARD_NO_OVERWRITE_USES"></a><a id="discard_no_overwrite_uses"></a>Common Usage of D3D10_MAP_WRITE_DISCARD with D3D10_MAP_WRITE_NO_OVERWRITE</h3>
D3D10_MAP_WRITE_DISCARD and D3D10_MAP_WRITE_NO_OVERWRITE are normally used in conjunction with dynamic index/vertex buffers, although they can also be used with dynamic textures.

A common use of these two flags involves filling dynamic index/vertex buffers with geometry that can be seen from the camera's current position. The first time that data is entered into the buffer on a given frame, Map is called with D3D10_MAP_WRITE_DISCARD; doing so invalidates the previous contents of the buffer. The buffer is then filled with all available data.

Subsequent writes to the buffer within the same frame should use D3D10_MAP_WRITE_NO_OVERWRITE. This will enable the CPU to access a resource that is potentially being used by the GPU as long as the restrictions described previously are respected.

## -see-also

<a href="/windows/win32/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
