---
UID: NS:d3d10.D3D10_QUERY_DATA_SO_STATISTICS
title: D3D10_QUERY_DATA_SO_STATISTICS
author: windows-sdk-content
description: Query information about the amount of data streamed out to the stream-output buffers in between ID3D10Asynchronous::Begin and ID3D10Asynchronous::End.
old-location: direct3d10\d3d10_query_data_so_statistics.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_so_statistics.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: D3D10_QUERY_DATA_SO_STATISTICS, D3D10_QUERY_DATA_SO_STATISTICS structure [Direct3D 10], cf410b92-83dc-df50-69b8-4970b24d4f1c, d3d10/D3D10_QUERY_DATA_SO_STATISTICS, direct3d10.d3d10_query_data_so_statistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_DATA_SO_STATISTICS
product: Windows
targetos: Windows
req.typenames: D3D10_QUERY_DATA_SO_STATISTICS
req.redist: 
---

# D3D10_QUERY_DATA_SO_STATISTICS structure


## -description


Query information about the amount of data streamed out to the stream-output buffers in between <a href="https://msdn.microsoft.com/en-us/library/Bb173501(v=VS.85).aspx">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb173502(v=VS.85).aspx">ID3D10Asynchronous::End</a>.


## -struct-fields




### -field NumPrimitivesWritten

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT64</a></b>

Number of primitives (that is, points, lines, and triangles) written to the stream-output buffers.


### -field PrimitivesStorageNeeded

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT64</a></b>

Number of primitives that would have been written to the stream-output buffers if there had been enough space for them all.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

