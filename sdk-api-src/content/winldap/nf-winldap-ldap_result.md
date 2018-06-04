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

# ldap_result function


## -description


The <b>ldap_result</b> function obtains the result of an asynchronous operation.


## -parameters




### -param ld [in]

The session handle.


### -param msgid [in]

The message ID of the operation, or the constant LDAP_RES_ANY if any result is required.


### -param all [in]

Specifies how many messages are retrieved in a single call to <b>ldap_result</b>. This parameter only has meaning for search results. Pass the constant LDAP_MSG_ONE (0x00) to retrieve one message at a time. Pass LDAP_MSG_ALL (0x01) to request that all results of a search be received before returning all results in a single chain. Pass LDAP_MSG_RECEIVED (0x02) to indicate that all results retrieved so far should be returned in the result chain.


### -param timeout [in]

A timeout that specifies how long, in seconds, to wait for results to be returned. A <b>NULL</b> value causes <b>ldap_result</b> to block until results are available. A timeout value of zero seconds specifies a polling behavior.


### -param res [out]

Contains the result(s) of the operation. Any results returned should be freed with a call to <a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>
    once they are no longer required by the application.


## -returns



If the function succeeds, it returns one of the following values to indicate the type of the first result in the <i>res</i> parameter. If the time-out expires, the function returns 0.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_result</b> function retrieves the result of a previous, asynchronously initiated operation. Be aware that, depending on the way it is called, <b>ldap_result</b> may actually return a list or "chain" of messages.

For connectionless LDAP, you must pass both an LDAP connection handle and a message ID to ensure that you get the correct results. The LDAP run time continues to send the request until it receives a response.

Multithreading: Calls to <b>ldap_result</b> are thread safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>
 

 

