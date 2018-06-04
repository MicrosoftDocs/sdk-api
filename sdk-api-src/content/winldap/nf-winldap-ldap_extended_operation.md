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

# ldap_extended_operation function


## -description


The <b>ldap_extended_operation</b> function enables you to pass extended LDAP operations to the server.


## -parameters




### -param ld [in]

The session handle.


### -param Oid [in]

A pointer to a null-terminated string that contains the dotted object identifier  text string that names the request.


### -param Data [in]

The arbitrary data required by the operation. If <b>NULL</b>, no data is sent to the server.


### -param ServerControls [in]

Optional. A list of LDAP server controls. Set this parameter to <b>NULL</b>, if not used.


### -param ClientControls [in]

Optional. A list of client controls. Set this parameter to <b>NULL</b>, if not used.


### -param MessageNumber [out]

The message ID for the request.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_extended_operation</b> function enables a client to send an extended request (free for all) to an LDAP 3 (or later) server. The functionality is open and the client request can be for any operation.

As an asynchronous function, <b>ldap_extended_operation</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

Because of the open nature of the request, the client must call 
<a href="https://msdn.microsoft.com/829ffb8f-150b-438a-bcbd-42f2e9c01479">ldap_close_extended_op</a> to terminate the request.

Multithreading: The <b>ldap_extended_operation</b> function is thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/829ffb8f-150b-438a-bcbd-42f2e9c01479">ldap_close_extended_op</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

