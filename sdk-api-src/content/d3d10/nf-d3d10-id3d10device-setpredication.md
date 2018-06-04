---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D10Device::SetPredication


## -description


Set a rendering predicate.


## -parameters




### -param pPredicate [in]

Type: <b><a href="https://msdn.microsoft.com/baf387c4-dd7a-4a05-a118-839499caec24">ID3D10Predicate</a>*</b>

Pointer to a predicate (see <a href="https://msdn.microsoft.com/baf387c4-dd7a-4a05-a118-839499caec24">ID3D10Predicate</a>). A <b>NULL</b> value indicates "no" predication; in this case, the value of PredicateValue is irrelevent but will be preserved for <a href="https://msdn.microsoft.com/20cafa97-0677-4660-a889-01e99668b04f">ID3D10Device::GetPredication</a>.


### -param PredicateValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.


## -returns



Returns nothing.




## -remarks



The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">ID3D10Asynchronous::End</a> are invalid.

This method is used to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting Predicate data of the Predicate is equal to the PredicateValue. However, some Predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of Predication is to allow an application to issue graphics commands without taking the performance hit of spinning, waiting for <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> to return. So, Predication can occur while <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. Another way to think of it: an application can also use Predication as a fallback, if it is possible that <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. If <b>ID3D10Asynchronous::GetData</b> returns S_OK, the application can skip calling the graphics commands manually with it's own application logic.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

