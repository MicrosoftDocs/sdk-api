---
UID: NS:d3d11.D3D11_QUERY_DATA_SO_STATISTICS
title: D3D11_QUERY_DATA_SO_STATISTICS
author: windows-sdk-content
description: Query information about the amount of data streamed out to the stream-output buffers in between ID3D11DeviceContext::Begin and ID3D11DeviceContext::End.
old-location: direct3d11\d3d11_query_data_so_statistics.htm
old-project: direct3d11
ms.assetid: f5fa2563-817b-4ccd-a2c8-60926fa7d082
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 595165cc-6026-e884-f8d4-b74f4fc8e939, D3D11_QUERY_DATA_SO_STATISTICS, D3D11_QUERY_DATA_SO_STATISTICS structure [Direct3D 11], d3d11/D3D11_QUERY_DATA_SO_STATISTICS, direct3d11.d3d11_query_data_so_statistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_QUERY_DATA_SO_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_QUERY_DATA_SO_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_QUERY_DATA_SO_STATISTICS structure


## -description


Query information about the amount of data streamed out to the stream-output buffers in between <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> and <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a>.


## -struct-fields




### -field NumPrimitivesWritten

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives (that is, points, lines, and triangles) written to the stream-output buffers.


### -field PrimitivesStorageNeeded

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives that would have been written to the stream-output buffers if there had been enough space for them all.


## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

