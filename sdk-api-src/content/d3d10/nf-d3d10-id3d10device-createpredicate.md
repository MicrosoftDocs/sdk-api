---
UID: NF:d3d10.ID3D10Device.CreatePredicate
title: ID3D10Device::CreatePredicate
author: windows-sdk-content
description: Creates a predicate.
old-location: direct3d10\id3d10device_createpredicate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createpredicate.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 2b30a615-97cf-d010-fc84-3802da398aee, CreatePredicate, CreatePredicate method [Direct3D 10], CreatePredicate method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreatePredicate method, ID3D10Device.CreatePredicate, ID3D10Device::CreatePredicate, d3d10/ID3D10Device::CreatePredicate, direct3d10.id3d10device_createpredicate
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
 - ID3D10Device.CreatePredicate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::CreatePredicate


## -description


Creates a predicate.


## -parameters




### -param pPredicateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172405(v=VS.85).aspx">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description where the type of query must be a D3D10_QUERY_SO_OVERFLOW_PREDICATE or D3D10_QUERY_OCCLUSION_PREDICATE (see <a href="https://msdn.microsoft.com/en-us/library/Bb172405(v=VS.85).aspx">D3D10_QUERY_DESC</a>).


### -param ppPredicate [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173822(v=VS.85).aspx">ID3D10Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="https://msdn.microsoft.com/en-us/library/Bb173822(v=VS.85).aspx">ID3D10Predicate Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

