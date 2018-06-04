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

# IFsrmCommittableCollection::Commit


## -description


Commits all the objects of the collection and returns the commit results for each 
    object.


## -parameters




### -param options [in]

One or more options to use when committing the collection of objects. For possible values, see the 
      <a href="https://msdn.microsoft.com/eb362bd8-c11f-404e-be54-0e16007494a7">FsrmCommitOptions</a> enumeration.


### -param results [out]

A collection of <b>HRESULT</b> values that correspond directly to the objects in the 
       collection. The <b>HRESULT</b> value indicates the success or failure of committing the 
       object.

If the method returns <b>FSRM_S_PARTIAL_BATCH</b> or 
       <b>FSRM_E_FAIL_BATCH</b>, check the results.


## -returns



The method returns the following return values.




## -remarks



Committing objects in a batch operation provides better performance than committing each object in the 
    collection individually (for example, calling the 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreen::Commit</a> method).

Note that the state of the objects in the collection must be the same. For example, the collection must 
    contain all new objects, objects marked for deletion, or modified objects. The modified category covers objects 
    are not new or marked for deletion—it does not necessarily mean that they've been 
    modified.

A collection of imported objects would be considered a collection of modified objects. If you marked one or 
    more of the imported objects for deletion (called the 
    <a href="https://msdn.microsoft.com/ce8a17fe-377b-4a0e-9a95-7dc25a1411ce">Delete</a> method on the object), you would first have to 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">remove</a> those objects from the collection before 
    committing the rest.




## -see-also




<a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a>
 

 

