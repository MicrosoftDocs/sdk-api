---
UID: NS:d3d10.D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
title: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
author: windows-sdk-content
description: Query information about the reliability of a timestamp query.
old-location: direct3d10\d3d10_query_data_timestamp_disjoint.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_timestamp_disjoint.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT, D3D10_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 10], d3d10/D3D10_QUERY_DATA_TIMESTAMP_DISJOINT, direct3d10.d3d10_query_data_timestamp_disjoint, ecae4d34-b796-887c-40aa-bb10d9b020bf
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
tech.root: 
req.typenames: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_QUERY_DATA_TIMESTAMP_DISJOINT structure


## -description


Query information about the reliability of a timestamp query.


## -struct-fields




### -field Frequency

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

How frequently the GPU counter increments in Hz.


### -field Disjoint

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If this is <b>TRUE</b>, something occurred in between the query's <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">ID3D10Asynchronous::End</a> calls that caused the timestamp counter to become discontinuous or disjoint, such as unplugging the AC chord on a laptop, overheating, or throttling up/down due to laptop savings events. The timestamp returned by <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> for a timestamp query is only reliable if Disjoint is <b>FALSE</b>.


## -remarks



For a list of query types see <a href="https://msdn.microsoft.com/f50197d6-48ba-498e-8c1b-9b0ae08a8782">D3D10_QUERY</a>.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

