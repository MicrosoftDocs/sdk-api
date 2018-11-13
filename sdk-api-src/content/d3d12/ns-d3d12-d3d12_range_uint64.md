---
UID: NS:d3d12.D3D12_RANGE_UINT64
title: D3D12_RANGE_UINT64
author: windows-sdk-content
description: Describes a memory range in a 64-bit address space.
old-location: direct3d12\d3d12_range_uint64.htm
tech.root: direct3d12
ms.assetid: 9A907848-285C-4489-8F53-DA02FBC0AC0C
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_RANGE_UINT64, D3D12_RANGE_UINT64 structure, d3d12/D3D12_RANGE_UINT64, direct3d12.d3d12_range_uint64
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
 - D3D12.h
api_name:
 - D3D12_RANGE_UINT64
product: Windows
targetos: Windows
req.typenames: D3D12_RANGE_UINT64
req.redist: 
---

# D3D12_RANGE_UINT64 structure


## -description


Describes a memory range in a 64-bit address space.


## -struct-fields




### -field Begin

The offset, in bytes, denoting the beginning of a memory range.


### -field End

The offset, in bytes, denoting the end of a memory range.
            <b>End</b> is one-past-the-end.


## -remarks



<b>End</b> is one-past-the-end.
        When <b>Begin</b> equals <b>End</b>, the range is empty.
        The size of the range is (<b>End</b> - <b>Begin</b>).
      

This structure is used by the <a href="https://msdn.microsoft.com/D8DACE22-9AFD-4DCD-A254-A34AD532ACD7">D3D12_SUBRESOURCE_RANGE_UINT64</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

