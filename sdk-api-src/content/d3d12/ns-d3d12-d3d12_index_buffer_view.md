---
UID: NS:d3d12.D3D12_INDEX_BUFFER_VIEW
title: D3D12_INDEX_BUFFER_VIEW
author: windows-sdk-content
description: Describes the index buffer to view.
old-location: direct3d12\d3d12_index_buffer_view.htm
old-project: direct3d12
ms.assetid: CADD98BF-EDA9-43D6-9ADA-392051541B61
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_INDEX_BUFFER_VIEW, D3D12_INDEX_BUFFER_VIEW structure, d3d12/D3D12_INDEX_BUFFER_VIEW, direct3d12.d3d12_index_buffer_view
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
req.typenames: D3D12_INDEX_BUFFER_VIEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_INDEX_BUFFER_VIEW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_INDEX_BUFFER_VIEW structure


## -description


Describes the index buffer to view.


## -struct-fields




### -field BufferLocation

The GPU virtual address of the index buffer.  
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd synonym of UINT64.
          


### -field SizeInBytes

The size in bytes of the index buffer.
          


### -field Format

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value for the index-buffer format.
          


## -remarks



This structure is passed into <a href="https://msdn.microsoft.com/EB776EC7-42F2-47D3-A1FA-771EC6C4E3AB">ID3D12GraphicsCommandList::IASetIndexBuffer</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

