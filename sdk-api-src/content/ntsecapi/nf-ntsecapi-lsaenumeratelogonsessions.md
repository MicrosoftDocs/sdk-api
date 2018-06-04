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

# LsaEnumerateLogonSessions function


## -description


The <b>LsaEnumerateLogonSessions</b> function retrieves the set of existing logon session identifiers (<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUIDs</a>) and the number of sessions.


## -parameters




### -param LogonSessionCount [out]

Pointer to a long integer that receives the number of elements returned in the array returned in <i>LogonSessionList</i> parameter.


### -param LogonSessionList [out]

Address of a pointer to a LUID. The pointer receives the first element of an array of logon session identifiers. The memory used by the array is allocated by the LSA. When the array is no longer needed, call the 
<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LSAFreeReturnBuffer</a> function to free it.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason.




## -remarks



To retrieve information about the logon sessions returned by <b>LsaEnumerateLogonSessions</b>, call the 
<a href="https://msdn.microsoft.com/b1478a7a-f508-4b98-8c7b-adeb2f07bb86">LsaGetLogonSessionData</a> function.



