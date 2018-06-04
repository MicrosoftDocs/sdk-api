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

# _POLICY_AUDIT_SID_ARRAY structure


## -description


The <b>POLICY_AUDIT_SID_ARRAY</b> structure specifies an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures that represent Windows users or groups.


## -struct-fields




### -field UsersCount

The number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures in the <b>UserSidArray</b> array.


### -field UserSidArray.size_is

 


### -field UserSidArray.size_is.UsersCount

 


### -field UserSidArray

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures that specify Windows users or groups.


## -see-also




<a href="https://msdn.microsoft.com/4b13f021-ba08-4eb8-9c7a-0512992ef272">AuditEnumeratePerUserPolicy</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

