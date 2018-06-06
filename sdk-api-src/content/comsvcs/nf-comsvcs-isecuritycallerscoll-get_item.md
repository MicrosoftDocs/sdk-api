---
UID: NF:comsvcs.ISecurityCallersColl.get_Item
title: ISecurityCallersColl::get_Item
author: windows-sdk-content
description: Retrieves a specified caller in the security callers collection.
old-location: cos\isecuritycallerscoll_get_item.htm
old-project: cossdk
ms.assetid: 24473ebe-8d29-46cd-817d-48f24b03c405
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ISecurityCallersColl interface [COM+],get_Item method, ISecurityCallersColl.get_Item, ISecurityCallersColl::get_Item, _cos_ISecurityCallersColl_get_Item, comsvcs/ISecurityCallersColl::get_Item, cos.isecuritycallerscoll_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ISecurityCallersColl interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallersColl.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

