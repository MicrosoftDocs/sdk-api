---
UID: NS:d3d12.D3D12_RESOURCE_ALLOCATION_INFO
title: D3D12_RESOURCE_ALLOCATION_INFO (d3d12.h)
author: windows-sdk-content
description: Describes parameters needed to allocate resources.
old-location: direct3d12\d3d12_resource_allocation_info.htm
tech.root: direct3d12
ms.assetid: ADBF5402-C1B5-4A10-92DF-E9F5706F52A1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_ALLOCATION_INFO, D3D12_RESOURCE_ALLOCATION_INFO structure, d3d12/D3D12_RESOURCE_ALLOCATION_INFO, direct3d12.d3d12_resource_allocation_info
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
 - D3D12_RESOURCE_ALLOCATION_INFO
product: Windows
targetos: Windows
req.typenames: D3D12_RESOURCE_ALLOCATION_INFO
req.redist: 
ms.custom: 19H1
---

# D3D12_RESOURCE_ALLOCATION_INFO structure


## -description


Describes parameters needed to allocate resources.


## -struct-fields




### -field SizeInBytes

The size, in bytes, of the resource.


### -field Alignment

The alignment value for the resource; one of 4KB (4096), 64KB (65536) and 4MB (4194304) alignment.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/43467E09-835B-4DB9-B0A4-F75868DE4609">GetResourceAllocationInfo</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/81FC8D0E-2C15-42D3-9E06-1FE193F707C6">CD3DX12_RESOURCE_ALLOCATION_INFO</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

