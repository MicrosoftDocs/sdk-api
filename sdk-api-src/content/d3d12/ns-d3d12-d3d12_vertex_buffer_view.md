---
UID: NS:d3d12.D3D12_VERTEX_BUFFER_VIEW
title: D3D12_VERTEX_BUFFER_VIEW
author: windows-sdk-content
description: Describes a vertex buffer view.
old-location: direct3d12\d3d12_vertex_buffer_view.htm
tech.root: direct3d12
ms.assetid: 7EFE1929-FCDD-48DD-99E4-135D8B515290
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_VERTEX_BUFFER_VIEW, D3D12_VERTEX_BUFFER_VIEW structure, d3d12/D3D12_VERTEX_BUFFER_VIEW, direct3d12.d3d12_vertex_buffer_view
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - d3d12.h
api_name:
 - D3D12_VERTEX_BUFFER_VIEW
product: Windows
targetos: Windows
req.typenames: D3D12_VERTEX_BUFFER_VIEW
req.redist: 
---

# D3D12_VERTEX_BUFFER_VIEW structure


## -description


Describes a vertex buffer view.


## -struct-fields




### -field BufferLocation

Specifies a D3D12_GPU_VIRTUAL_ADDRESS that identifies the address of the buffer.


### -field SizeInBytes

Specifies the size in bytes of the buffer.


### -field StrideInBytes

Specifies the size in bytes of each vertex entry.


## -remarks



Use this structure with the <a href="https://msdn.microsoft.com/AADD6CEF-376D-43AB-86E6-37B5D7DD0B25">IASetVertexBuffers</a> method.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

