---
UID: NS:d3d12.D3D12_BUFFER_SRV
title: D3D12_BUFFER_SRV
author: windows-sdk-content
description: Describes the elements in a buffer resource to use in a shader-resource view.
old-location: direct3d12\d3d12_buffer_srv.htm
old-project: direct3d12
ms.assetid: FD5FBA65-4C70-487F-8D93-0EC5668BCE4A
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_BUFFER_SRV, D3D12_BUFFER_SRV structure, d3d12/D3D12_BUFFER_SRV, direct3d12.d3d12_buffer_srv
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
tech.root: 
req.typenames: D3D12_BUFFER_SRV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_BUFFER_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_BUFFER_SRV structure


## -description


Describes the elements in a buffer resource to use in a shader-resource view.


## -struct-fields




### -field FirstElement

The index of the first element to be accessed by the view.


### -field NumElements

The number of elements in the resource.


### -field StructureByteStride

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer.


### -field Flags


            A <a href="https://msdn.microsoft.com/153F82A2-077A-4D42-8FC3-C3370999AF6C">D3D12_BUFFER_SRV_FLAGS</a>-typed value that identifies view options for the buffer. Currently, the only option is to identify a raw view of the buffer. For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/9e991ab0-9648-484a-9a2c-5391ee5abf20">Raw Views of Buffers</a>.
          


## -remarks




          This structure is used by <a href="https://msdn.microsoft.com/2B4B868F-3E9F-4570-B1C7-2767ED717A3B">D3D12_SHADER_RESOURCE_VIEW_DESC</a> to create a view of a buffer.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

