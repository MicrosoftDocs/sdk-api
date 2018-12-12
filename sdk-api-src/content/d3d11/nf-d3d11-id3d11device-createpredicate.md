---
UID: NF:d3d11.ID3D11Device.CreatePredicate
title: ID3D11Device::CreatePredicate
author: windows-sdk-content
description: Creates a predicate.
old-location: direct3d11\id3d11device_createpredicate.htm
tech.root: direct3d11
ms.assetid: 5af4e63b-ba85-4c73-82e3-b09579d7ce78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 3892a0ec-dd05-6f9e-18d3-d6cc2cc95d5f, CreatePredicate, CreatePredicate method [Direct3D 11], CreatePredicate method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreatePredicate method, ID3D11Device.CreatePredicate, ID3D11Device::CreatePredicate, d3d11/ID3D11Device::CreatePredicate, direct3d11.id3d11device_createpredicate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreatePredicate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CreatePredicate


## -description


Creates a predicate.


## -parameters




### -param pPredicateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/2ed8e380-744b-41e1-87c8-9c7e8100ea2f">D3D11_QUERY_DESC</a>*</b>

Pointer to a query description where the type of query must be a D3D11_QUERY_SO_OVERFLOW_PREDICATE or D3D11_QUERY_OCCLUSION_PREDICATE (see <a href="https://msdn.microsoft.com/2ed8e380-744b-41e1-87c8-9c7e8100ea2f">D3D11_QUERY_DESC</a>).


### -param ppPredicate [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

