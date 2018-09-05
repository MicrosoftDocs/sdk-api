---
UID: NF:d3d10.ID3D10Device.CreateQuery
title: ID3D10Device::CreateQuery
author: windows-sdk-content
description: This interface encapsulates methods for querying information from the GPU.
old-location: direct3d10\id3d10device_createquery.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createquery.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateQuery, CreateQuery method [Direct3D 10], CreateQuery method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateQuery method, ID3D10Device.CreateQuery, ID3D10Device::CreateQuery, d3d10/ID3D10Device::CreateQuery, direct3d10.id3d10device_createquery, e041861e-bdae-c4f9-1ea4-d5af2d5b38ab
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateQuery
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateQuery


## -description


This interface encapsulates methods for querying information from the GPU.


## -parameters




### -param pQueryDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description (see <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>).


### -param ppQuery [out]

Type: <b><a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query</a>**</b>

Address of a pointer to the query object created (see <a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

