---
UID: NE:d3d9types._D3DQUERYTYPE
title: "_D3DQUERYTYPE"
author: windows-driver-content
description: Identifies the query type.
old-location: direct3d9\D3DQUERYTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dquerytype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DQUERYTYPE, D3DQUERYTYPE enumeration [Direct3D 9], D3DQUERYTYPE_BANDWIDTHTIMINGS, D3DQUERYTYPE_CACHEUTILIZATION, D3DQUERYTYPE_EVENT, D3DQUERYTYPE_INTERFACETIMINGS, D3DQUERYTYPE_MEMORYPRESSURE, D3DQUERYTYPE_OCCLUSION, D3DQUERYTYPE_PIPELINETIMINGS, D3DQUERYTYPE_PIXELTIMINGS, D3DQUERYTYPE_ResourceManager, D3DQUERYTYPE_TIMESTAMP, D3DQUERYTYPE_TIMESTAMPDISJOINT, D3DQUERYTYPE_TIMESTAMPFREQ, D3DQUERYTYPE_VCACHE, D3DQUERYTYPE_VERTEXSTATS, D3DQUERYTYPE_VERTEXTIMINGS, LPD3DQUERYTYPE, LPD3DQUERYTYPE enumeration pointer [Direct3D 9], _D3DQUERYTYPE, a35e11b0-01e1-a68e-2080-b2ae5718ce1c, d3d9types/D3DQUERYTYPE, d3d9types/D3DQUERYTYPE_BANDWIDTHTIMINGS, d3d9types/D3DQUERYTYPE_CACHEUTILIZATION, d3d9types/D3DQUERYTYPE_EVENT, d3d9types/D3DQUERYTYPE_INTERFACETIMINGS, d3d9types/D3DQUERYTYPE_MEMORYPRESSURE, d3d9types/D3DQUERYTYPE_OCCLUSION, d3d9types/D3DQUERYTYPE_PIPELINETIMINGS, d3d9types/D3DQUERYTYPE_PIXELTIMINGS, d3d9types/D3DQUERYTYPE_ResourceManager, d3d9types/D3DQUERYTYPE_TIMESTAMP, d3d9types/D3DQUERYTYPE_TIMESTAMPDISJOINT, d3d9types/D3DQUERYTYPE_TIMESTAMPFREQ, d3d9types/D3DQUERYTYPE_VCACHE, d3d9types/D3DQUERYTYPE_VERTEXSTATS, d3d9types/D3DQUERYTYPE_VERTEXTIMINGS, d3d9types/LPD3DQUERYTYPE, direct3d9.D3DQUERYTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DQUERYTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DQUERYTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DQUERYTYPE enumeration


## -description


Identifies the query type. For information about queries, see <a href="https://msdn.microsoft.com/2c65d199-141d-43a7-b513-4cb4459d7c27">Queries (Direct3D 9)</a>



## -enum-fields




### -field D3DQUERYTYPE_VCACHE

Query for driver hints about data layout for vertex caching.


### -field D3DQUERYTYPE_RESOURCEMANAGER


### -field D3DQUERYTYPE_VERTEXSTATS

Query vertex statistics.


### -field D3DQUERYTYPE_EVENT

Query for any and all asynchronous events that have been issued from API calls. 


### -field D3DQUERYTYPE_OCCLUSION

An occlusion query returns the number of pixels that pass z-testing. These pixels are for primitives drawn between the issue of <a href="https://msdn.microsoft.com/21b8a2b0-d18f-4412-b655-3a913b7312ee">D3DISSUE_BEGIN</a> and <a href="https://msdn.microsoft.com/9ced932a-5d98-4bf8-aa11-06560f53546d">D3DISSUE_END</a>. This enables an application to check the occlusion result against 0. Zero is fully occluded, which means the pixels are not visible from the current camera position.


### -field D3DQUERYTYPE_TIMESTAMP

Returns a 64-bit timestamp.


### -field D3DQUERYTYPE_TIMESTAMPDISJOINT

Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE_TIMESTAMP.


### -field D3DQUERYTYPE_TIMESTAMPFREQ

This query result is <b>TRUE</b> if the values from D3DQUERYTYPE_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE_TIMESTAMPDISJOINT query. Otherwise, the query result is <b>FALSE</b>.


### -field D3DQUERYTYPE_PIPELINETIMINGS

Percent of time processing pipeline data.


### -field D3DQUERYTYPE_INTERFACETIMINGS

Percent of time processing data in the driver.


### -field D3DQUERYTYPE_VERTEXTIMINGS

Percent of time processing vertex shader data.


### -field D3DQUERYTYPE_PIXELTIMINGS

Percent of time processing pixel shader data.


### -field D3DQUERYTYPE_BANDWIDTHTIMINGS

Throughput measurement comparisons for help in understanding the performance of an application.


### -field D3DQUERYTYPE_CACHEUTILIZATION

Measure the cache hit-rate performance for textures and indexed vertices.


### -field D3DQUERYTYPE_MEMORYPRESSURE

Efficiency of memory allocation contained in a  <a href="https://msdn.microsoft.com/bdf65d35-281f-4795-a2c1-0d4e91bfa7bc">D3DMEMORYPRESSURE</a> structure.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

D3DQUERYTYPE_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).

</td>
</tr>
</table>
 


#### - D3DQUERYTYPE_ResourceManager

Query the resource manager. For this query, the device behavior flags must include <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd"> D3DCREATE_DISABLE_DRIVER_MANAGEMENT</a>.


## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/0733a30e-b142-46cd-a8b5-3f70ced77521">IDirect3DDevice9::CreateQuery</a>
 

 

