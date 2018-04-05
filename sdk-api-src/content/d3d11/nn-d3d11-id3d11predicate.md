---
UID: NN:d3d11.ID3D11Predicate
title: ID3D11Predicate
author: windows-driver-content
description: A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.
old-location: direct3d11\id3d11predicate.htm
old-project: direct3d11
ms.assetid: ad16e0ac-a5ff-41ae-9b73-e93235ef891b
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 7bbde1c2-0bd3-3fda-2288-938ac2c04c3a, ID3D11Predicate, ID3D11Predicate interface [Direct3D 11], ID3D11Predicate interface [Direct3D 11], described, d3d11/ID3D11Predicate, direct3d11.id3d11predicate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	ID3D11Predicate
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Predicate interface


## -description


A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.


## -remarks



To create a predicate object, call <a href="https://msdn.microsoft.com/5af4e63b-ba85-4c73-82e3-b09579d7ce78">ID3D11Device::CreatePredicate</a>. To set the predicate object, call <a href="https://msdn.microsoft.com/ceac248a-31c9-4e14-892f-f047e288daae">ID3D11DeviceContext::SetPredication</a>.

There are two types of predicates: stream-output-overflow predicates and occlusion predicates. Stream-output-overflow predicates cause any geometry residing in stream-output buffers that were overflowed to not be processed. Occlusion predicates cause any geometry that did not have a single sample pass the depth/stencil tests to not be processed.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a>
 

 

