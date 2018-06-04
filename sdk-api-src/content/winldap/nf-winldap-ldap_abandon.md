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

# ldap_abandon function


## -description


A client calls <b>ldap_abandon</b> to cancel an in-process asynchronous LDAP call.


## -parameters




### -param ld [in]

The session handle.


### -param msgid [in]

The message ID of the call to be canceled. Asynchronous functions, such as <a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a> and <a href="https://msdn.microsoft.com/93ae0af4-1b16-4bb0-952f-139241189d79">ldap_modify</a>,  return this message ID when they initiate an operation.


## -returns



If the function succeeds, that is, if the cancel operation is successful, the return value is zero.

If the function fails, the return value is –1.




## -remarks



The <b>ldap_abandon</b> function first verifies that the operation has been completed. If it has, the message ID is deleted; otherwise, the call goes to the server to cancel the operation. Be aware that a successful call to <b>ldap_abandon</b> destroys the message ID. Therefore, you cannot call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> to obtain results with that message ID, even if the server completed the operation.

There is no server response to <b>ldap_abandon</b>; thus, there is no guarantee that the call reached the server.

Multithreading: Calls to <b>ldap_abandon</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

