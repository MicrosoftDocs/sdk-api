---
UID: NE:d3d10.D3D10_QUERY
title: D3D10_QUERY
author: windows-sdk-content
description: Query types.
old-location: direct3d10\d3d10_query.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_QUERY, D3D10_QUERY enumeration [Direct3D 10], D3D10_QUERY_EVENT, D3D10_QUERY_OCCLUSION, D3D10_QUERY_OCCLUSION_PREDICATE, D3D10_QUERY_PIPELINE_STATISTICS, D3D10_QUERY_SO_OVERFLOW_PREDICATE, D3D10_QUERY_SO_STATISTICS, D3D10_QUERY_TIMESTAMP, D3D10_QUERY_TIMESTAMP_DISJOINT, d3d10/D3D10_QUERY, d3d10/D3D10_QUERY_EVENT, d3d10/D3D10_QUERY_OCCLUSION, d3d10/D3D10_QUERY_OCCLUSION_PREDICATE, d3d10/D3D10_QUERY_PIPELINE_STATISTICS, d3d10/D3D10_QUERY_SO_OVERFLOW_PREDICATE, d3d10/D3D10_QUERY_SO_STATISTICS, d3d10/D3D10_QUERY_TIMESTAMP, d3d10/D3D10_QUERY_TIMESTAMP_DISJOINT, direct3d10.d3d10_query, e40f5532-bdd2-10c8-b69c-1b328c82ae9c
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D3D10_QUERY
product: Windows
targetos: Windows
req.typenames: D3D10_QUERY
req.redist: 
---

# D3D10_QUERY enumeration


## -description


Query types.


## -enum-fields




### -field D3D10_QUERY_EVENT

Determines whether or not the GPU is finished processing commands. When the GPU is finished processing commands <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> will return S_OK, and pData will point to a BOOL with a value of <b>TRUE</b>. When using this type of query, <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> is disabled.


### -field D3D10_QUERY_OCCLUSION

Get the number of samples that passed the depth and stencil tests in between <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">End</a>. <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> returns a UINT64. If a depth or stencil test is disabled, then each of those tests will be counted as a pass.


### -field D3D10_QUERY_TIMESTAMP

Get a timestamp value where <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> returns a UINT64. This kind of query is only useful if two timestamp queries are done in the middle of a D3D10_QUERY_TIMESTAMP_DISJOINT query. The difference of two timestamps can be used to determine how many ticks have elapsed, and the D3D10_QUERY_TIMESTAMP_DISJOINT query will determine if that difference is a reliable value and also has a value that shows how to convert the number of ticks into seconds. See <a href="https://msdn.microsoft.com/16cb5233-9e7e-4b1c-a231-4d949414a774">D3D10_QUERY_DATA_TIMESTAMP_DISJOINT</a>. When using this type of query, <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> is disabled.


### -field D3D10_QUERY_TIMESTAMP_DISJOINT

Determines whether or not a D3D10_QUERY_TIMESTAMP is returning reliable values, and also gives the frequency of the processor enabling you to convert the number of elapsed ticks into seconds. <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> will return a <a href="https://msdn.microsoft.com/16cb5233-9e7e-4b1c-a231-4d949414a774">D3D10_QUERY_DATA_TIMESTAMP_DISJOINT</a>. This type of query should only be invoked once per frame or less.


### -field D3D10_QUERY_PIPELINE_STATISTICS

Get pipeline statistics, such as the number of pixel shader invocations in between <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">End</a>. <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> will return a <a href="https://msdn.microsoft.com/ade3cfee-a5b1-4873-9a5d-7d19082fe537">D3D10_QUERY_DATA_PIPELINE_STATISTICS</a>.


### -field D3D10_QUERY_OCCLUSION_PREDICATE

Similar to D3D10_QUERY_OCCLUSION, except <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> returns a BOOL indicating whether or not any samples passed the depth and stencil tests - <b>TRUE</b> meaning at least one passed, <b>FALSE</b> meaning none passed.


### -field D3D10_QUERY_SO_STATISTICS

Get streaming output statistics, such as the number of primitives streamed out in between <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">End</a>. <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> will return a <a href="https://msdn.microsoft.com/d6b17d1a-794e-4b35-ab9c-bf058e2e9ac6">D3D10_QUERY_DATA_SO_STATISTICS</a> structure.


### -field D3D10_QUERY_SO_OVERFLOW_PREDICATE

Determines whether or not any of the streaming output buffers overflowed in between <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">End</a>. <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.


## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

