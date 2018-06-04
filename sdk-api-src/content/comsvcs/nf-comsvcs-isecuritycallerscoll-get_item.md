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

# ISecurityCallersColl::get_Item


## -description


Retrieves a specified caller in the security callers collection.


## -parameters




### -param lIndex [in]

The name of the caller to retrieve. See Remarks for information about the available callers.


### -param pObj [out]

A reference to the retrieved caller.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The security callers collection represents a chain of callers that cross security boundaries. These callers are also known as upstream callers.

Each item in this collection is a <a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a> object. To obtain an item in this collection, use the Item property of the <a href="https://msdn.microsoft.com/164fe12d-eeb3-402f-8aa3-e3545904d9c4">SecurityCallers</a> collection object, specifying an integer index value between 0 and the number of callers, minus 1, in the collection. To retrieve the direct caller, this index value should be 0, and to retrieve the original caller, the index can be either -1 or the number of callers minus 1.




## -see-also




<a href="https://msdn.microsoft.com/b9b16d2e-92fd-40d2-b33d-8a82a1291794">ISecurityCallersColl</a>
 

 

