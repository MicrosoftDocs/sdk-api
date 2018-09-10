---
UID: NF:d3d10.ID3D10Device.CreateQuery
title: ID3D10Device::CreateQuery
author: windows-sdk-content
description: This interface encapsulates methods for querying information from the GPU.
old-location: direct3d10\id3d10device_createquery.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createquery.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateQuery, CreateQuery method [Direct3D 10], CreateQuery method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateQuery method, ID3D10Device.CreateQuery, ID3D10Device::CreateQuery, d3d10/ID3D10Device::CreateQuery, direct3d10.id3d10device_createquery, e041861e-bdae-c4f9-1ea4-d5af2d5b38ab
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D10Device::CreateQuery


## -description


This interface encapsulates methods for querying information from the GPU.


## -parameters




### -param pQueryDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172405(v=VS.85).aspx">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172405(v=VS.85).aspx">D3D10_QUERY_DESC</a>).


### -param ppQuery [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173823(v=VS.85).aspx">ID3D10Query</a>**</b>

Address of a pointer to the query object created (see <a href="https://msdn.microsoft.com/en-us/library/Bb173823(v=VS.85).aspx">ID3D10Query Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

