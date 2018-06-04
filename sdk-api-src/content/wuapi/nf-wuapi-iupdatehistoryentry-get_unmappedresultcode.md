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

# IUpdateHistoryEntry::get_UnmappedResultCode


## -description


Gets the unmapped result code that is returned from an operation on an update.

This property is read-only.


## -parameters


## -remarks



The returned value is an unmapped result code. To retrieve a mapped exception code, use the <a href="https://msdn.microsoft.com/7e1968f9-548c-4002-848b-9443d12ea0a7">HResult</a> property.




## -see-also




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>



<a href="https://msdn.microsoft.com/7e1968f9-548c-4002-848b-9443d12ea0a7">IUpdateHistoryEntry.HResult</a>



<a href="https://msdn.microsoft.com/4dfad46b-ee42-41d6-be25-69aaf12fd53c">IUpdateHistoryEntry.Operation</a>
 

 

