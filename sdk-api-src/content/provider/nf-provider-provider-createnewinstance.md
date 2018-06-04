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

# Provider::CreateNewInstance


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CreateNewInstance</b> method allocates a new <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> object and returns a pointer to it.


## -parameters




### -param pMethodContext

A pointer to the context associated with this instance.


## -returns



Returns a pointer to the new instance.




## -remarks



The caller must call either CInstance::Release or <a href="https://msdn.microsoft.com/619adf78-26db-4a90-90ba-bdacb3e55975">Provider::Commit</a> on the returned pointer. Either of these methods may be used, but they are not interchangeable. Refer to the Remarks section on each of these methods to determine which is appropriate.

This method does not return a <b>NULL</b> pointer. If it fails, it throws an exception.



