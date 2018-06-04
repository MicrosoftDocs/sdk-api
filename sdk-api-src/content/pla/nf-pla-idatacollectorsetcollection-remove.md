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

# IDataCollectorSetCollection::Remove


## -description


Removes a data collector set from the collection.


## -parameters




### -param set






#### - vSet [in]

The zero-based index of the data collector set to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a> to be removed.

Note that by removing the set from the collection, you are also deleting the set from the hard disk.




## -see-also




<a href="https://msdn.microsoft.com/5f4cc411-1efb-4f70-a677-3c20d95f0c53">IDataCollectorSetCollection</a>



<a href="https://msdn.microsoft.com/c551e373-77a4-4bac-848d-5aaec1e89cf1">IDataCollectorSetCollection::Add</a>



<a href="https://msdn.microsoft.com/a7a4754c-8c64-4add-89b1-c5bdbf4cb807">IDataCollectorSetCollection::Clear</a>
 

 

