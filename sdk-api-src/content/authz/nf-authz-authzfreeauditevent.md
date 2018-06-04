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

# AuthzFreeAuditEvent function


## -description


The <b>AuthzFreeAuditEvent</b> function frees the  structure allocated by the 
<a href="https://msdn.microsoft.com/cf79a92f-31e0-47cf-8990-4dbd46056a90">AuthzInitializeObjectAccessAuditEvent</a> function.


## -parameters




### -param hAuditEvent

TBD




#### - pAuditEventInfo [in]

A pointer to the <b>AUTHZ_AUDIT_EVENT_HANDLE</b> structure to be freed.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf79a92f-31e0-47cf-8990-4dbd46056a90">AuthzInitializeObjectAccessAuditEvent</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

