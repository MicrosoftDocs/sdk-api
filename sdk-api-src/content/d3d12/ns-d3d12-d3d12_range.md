---
UID: NS:d3d12.D3D12_RANGE
title: D3D12_RANGE
author: windows-sdk-content
description: Describes a memory range.
old-location: direct3d12\d3d12_range.htm
tech.root: direct3d12
ms.assetid: E8A66EC7-DB20-475D-BCD1-6C164FF39D24
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_RANGE, D3D12_RANGE structure, d3d12/D3D12_RANGE, direct3d12.d3d12_range
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
 - D3D12_RANGE
product: Windows
targetos: Windows
req.typenames: D3D12_RANGE
req.redist: 
---

# D3D12_RANGE structure


## -description


Describes a memory range.


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
      

This structure is used by the <a href="https://msdn.microsoft.com/71E43B63-9C84-4E4B-A43D-92B958C8AAF5">Map</a> and <a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a> methods.
      




## -see-also




<a href="https://msdn.microsoft.com/5D5192BF-D14C-487B-A214-F8428E82AF0E">CD3DX12_RANGE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

