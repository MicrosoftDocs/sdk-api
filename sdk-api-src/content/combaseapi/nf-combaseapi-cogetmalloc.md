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

# CoGetMalloc function


## -description


Retrieves a pointer to the default OLE task memory allocator (which supports the system implementation of the <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface) so applications can call its methods to manage memory.


## -parameters




### -param dwMemContext [in]

This parameter must be 1.


### -param ppMalloc [out]

The address of an <b>IMalloc*</b> pointer variable that receives the interface pointer to the memory allocator.


## -returns



This function can return the standard return values S_OK, E_INVALIDARG, and E_OUTOFMEMORY.




## -remarks



The pointer to the <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface pointer received through the <i>ppMalloc</i> parameter cannot be used from a remote process; each process must have its own allocator.





## -see-also




<a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>



<a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a>
 

 

