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

# ldap_close_extended_op function


## -description


The <b>ldap_close_extended_op</b> function ends a request that was made by calling 
<a href="https://msdn.microsoft.com/02dda7c5-9779-4390-9395-aa917fa82546">ldap_extended_operation</a>.


## -parameters




### -param ld [in]

The session handle.


### -param MessageNumber [in]

The message ID for the request.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



After sending an extended request, or a series of such requests, to an LDAP server, call <b>ldap_close_extended_op</b> to notify the server that the client has finished making requests. Be aware that these extended operation functions are available only with LDAP, version 3 or later. These functions allow a client to send a "free-for-all" request, for any sort of data or action, to an LDAP 3 server.

Multithreading: Calls to <b>ldap_close_extended_op</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/02dda7c5-9779-4390-9395-aa917fa82546">ldap_extended_operation</a>
 

 

