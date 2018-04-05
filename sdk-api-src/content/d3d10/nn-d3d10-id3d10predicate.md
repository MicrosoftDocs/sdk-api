---
UID: NN:d3d10.ID3D10Predicate
title: ID3D10Predicate
author: windows-driver-content
description: A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.
old-location: direct3d10\id3d10predicate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10predicate.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 350beb86-4869-80f7-d757-00ebb1191143, ID3D10Predicate, ID3D10Predicate interface [Direct3D 10], ID3D10Predicate interface [Direct3D 10], described, d3d10/ID3D10Predicate, direct3d10.id3d10predicate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Predicate
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Predicate interface


## -description


A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.


## -remarks



A predicate can be created with <a href="https://msdn.microsoft.com/472d782b-a9ea-49b2-8489-4e074e48c15e">ID3D10Device::CreatePredicate</a>, and used with <a href="https://msdn.microsoft.com/175c4905-834a-4f18-bbf6-3bbe20e06d4d">ID3D10Device::SetPredication</a>.

There are two types of predicates in Direct3D 10: stream-output-overflow predicates and occlusion predicates. Stream-output-overflow predicates will cause any geometry residing in stream-output buffers that were overflowed to not be processed. Occlusion predicates will cause any geometry that did not have a single sample pass the depth/stencil tests to not be processed.

For an example of occlusion-predicated rendering, see <a href="6677cf3c-c360-49f4-c8e5-b1664f783dc0">Draw Predicated Sample</a>. 




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query</a>
 

 

