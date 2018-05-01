---
UID: NF:d3d11.ID3D11DeviceContext.GetPredication
title: ID3D11DeviceContext::GetPredication method
author: windows-driver-content
description: Get the rendering predicate state.
old-location: direct3d11\id3d11devicecontext_getpredication.htm
old-project: direct3d11
ms.assetid: 9a283895-51c4-4de5-bdeb-994f3085bd79
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: GetPredication method [Direct3D 11], GetPredication method [Direct3D 11], ID3D11DeviceContext interface, GetPredication,ID3D11DeviceContext.GetPredication, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], GetPredication method, ID3D11DeviceContext::GetPredication, ae323354-9c3a-634f-4e86-882e408d29d5, d3d11/ID3D11DeviceContext::GetPredication, direct3d11.id3d11devicecontext_getpredication
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.GetPredication
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::GetPredication method


## -description


Get the rendering predicate state.


## -parameters




### -param ppPredicate [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>). Value stored here will be <b>NULL</b> upon device creation.


### -param pPredicateValue [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Address of a boolean to fill with the predicate comparison value. <b>FALSE</b> upon device creation.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

