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

# AuthzRegisterSecurityEventSource function


## -description


The <b>AuthzRegisterSecurityEventSource</b> function registers a security event source with the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA).


## -parameters




### -param dwFlags [in]

This parameter is reserved for future use. Set this parameter to zero.


### -param szEventSourceName [in]

A pointer to the name of the security event source to register.


### -param phEventProvider [out]

A pointer to a handle to the registered security event source.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function  validates the <i>szEventSourceName</i> parameter  and sets up the appropriate structures and RPC connections to log events with that source name.  The validation is handled by an underlying call to an LSA API.  

The LSA API  verifies the following:

<ul>
<li>The caller has the  SeAuditPrivilege access right.</li>
<li>The event source is not already in use.</li>
<li>The event source is registered.</li>
<li>The calling application matches the executable image path in the event source registration, if one exists.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ca3086b-f9c9-4305-aaf3-c41b5dba30ad">AuthzUnregisterSecurityEventSource</a>
 

 

