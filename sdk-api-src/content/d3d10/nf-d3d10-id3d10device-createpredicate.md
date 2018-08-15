---
UID: NF:d3d10.ID3D10Device.CreatePredicate
title: ID3D10Device::CreatePredicate
author: windows-sdk-content
description: Creates a predicate.
old-location: direct3d10\id3d10device_createpredicate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createpredicate.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2b30a615-97cf-d010-fc84-3802da398aee, CreatePredicate, CreatePredicate method [Direct3D 10], CreatePredicate method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreatePredicate method, ID3D10Device.CreatePredicate, ID3D10Device::CreatePredicate, d3d10/ID3D10Device::CreatePredicate, direct3d10.id3d10device_createpredicate
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
 - ID3D10Device.CreatePredicate
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreatePredicate


## -description


Creates a predicate.


## -parameters




### -param pPredicateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description where the type of query must be a D3D10_QUERY_SO_OVERFLOW_PREDICATE or D3D10_QUERY_OCCLUSION_PREDICATE (see <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>).


### -param ppPredicate [out]

Type: <b><a href="https://msdn.microsoft.com/baf387c4-dd7a-4a05-a118-839499caec24">ID3D10Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="https://msdn.microsoft.com/baf387c4-dd7a-4a05-a118-839499caec24">ID3D10Predicate Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

