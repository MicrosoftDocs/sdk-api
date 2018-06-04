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

# AuthzOpenObjectAudit function


## -description


The <b>AuthzOpenObjectAudit</b> function reads the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the specified security descriptor and generates any appropriate audits specified by that SACL.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param hAuthzClientContext [in]

A handle to the client context of the object to open.


### -param pRequest [in]

A pointer to an 
<a href="https://msdn.microsoft.com/3748075c-b31a-4669-b8a6-1a540449d8fa">AUTHZ_ACCESS_REQUEST</a> structure.


### -param hAuditEvent [in]

A handle to the audit event to use.


### -param pSecurityDescriptor [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure for the object.


### -param OPTIONAL

TBD


### -param OptionalSecurityDescriptorCount

TBD


### -param pReply [in]

A pointer to an 
<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a> structure.


#### - SecurityDescriptorArray [in]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structures.


#### - SecurityDescriptorCount [in]

The number of elements in <i>SecurityDescriptorArray</i>. 

					


## -returns



If the function succeeds, it returns a nonzero value. 

If the function fails, it returns a zero value. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

