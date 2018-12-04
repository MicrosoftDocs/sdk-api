---
UID: NS:d3d12.D3D12_MEMCPY_DEST
title: D3D12_MEMCPY_DEST
author: windows-sdk-content
description: Describes the destination of a memory copy operation.
old-location: direct3d12\d3d12_memcpy_dest.htm
tech.root: direct3d12
ms.assetid: B85B7B60-FA34-4A4D-B1A7-D54884956E83
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_MEMCPY_DEST, D3D12_MEMCPY_DEST structure, d3d12/D3D12_MEMCPY_DEST, direct3d12.d3d12_memcpy_dest
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12.h
api_name:
 - D3D12_MEMCPY_DEST
product: Windows
targetos: Windows
req.typenames: D3D12_MEMCPY_DEST
req.redist: 
---

# D3D12_MEMCPY_DEST structure


## -description


Describes the destination of a memory copy operation.
      


## -struct-fields




### -field pData

A pointer to a memory block that receives the copied data.
          


### -field RowPitch

The row pitch, or width, or physical size, in bytes, of the subresource data.
          


### -field SlicePitch

The slice pitch, or width, or physical size, in bytes, of the subresource data.
          


## -remarks



This structure is used by a number of helper methods, refer to <a href="https://msdn.microsoft.com/095958A9-345B-45AE-8363-B353534044B2">Helper Structures and Functions for D3D12</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

