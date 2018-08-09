---
UID: NS:d3d12.D3D12_QUERY_DATA_SO_STATISTICS
title: D3D12_QUERY_DATA_SO_STATISTICS
author: windows-sdk-content
description: Describes query data for stream output.
old-location: direct3d12\d3d12_query_data_so_statistics.htm
old-project: direct3d12
ms.assetid: 7A71F6DA-AAC2-4070-90E9-F91F090AD1A1
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_QUERY_DATA_SO_STATISTICS, D3D12_QUERY_DATA_SO_STATISTICS structure, d3d12/D3D12_QUERY_DATA_SO_STATISTICS, direct3d12.d3d12_query_data_so_statistics
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
req.typenames: D3D12_QUERY_DATA_SO_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_QUERY_DATA_SO_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_QUERY_DATA_SO_STATISTICS structure


## -description


Describes query data for stream output.


## -struct-fields




### -field NumPrimitivesWritten

Specifies the number of primitives written.


### -field PrimitivesStorageNeeded

Specifies the total amount of storage needed by the primitives.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/FDD5F81B-F356-49D9-B6FE-FE2847934E61">D3D12_QUERY_HEAP_TYPE</a> and <a href="https://msdn.microsoft.com/98B238D0-8E4D-46C1-AC2C-09473A972E71">CreateQueryHeap</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

