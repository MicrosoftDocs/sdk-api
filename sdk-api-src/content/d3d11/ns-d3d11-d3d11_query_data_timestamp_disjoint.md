---
UID: NS:d3d11.D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
title: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
author: windows-sdk-content
description: Query information about the reliability of a timestamp query.
old-location: direct3d11\d3d11_query_data_timestamp_disjoint.htm
tech.root: direct3d11
ms.assetid: d706626a-cf11-4087-b66a-350161050aad
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT, D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 11], d3d11/D3D11_QUERY_DATA_TIMESTAMP_DISJOINT, direct3d11.d3d11_query_data_timestamp_disjoint, f6339efd-3b83-c410-71de-6ecde51119d9
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
product: Windows
targetos: Windows
req.typenames: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
req.redist: 
---

# D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure


## -description


Query information about the reliability of a timestamp query.


## -struct-fields




### -field Frequency

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

How frequently the GPU counter increments in Hz.


### -field Disjoint

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If this is <b>TRUE</b>, something occurred in between the query's <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> and <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> calls that caused the timestamp counter to become discontinuous or disjoint, such as unplugging the AC cord on a laptop, overheating, or throttling up/down due to laptop savings events. The timestamp returned by <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> for a timestamp query is only reliable if <b>Disjoint</b> is <b>FALSE</b>.


## -remarks



For a list of query types see <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11_QUERY</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

