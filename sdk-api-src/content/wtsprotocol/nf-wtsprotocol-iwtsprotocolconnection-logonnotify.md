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

# IWTSProtocolConnection::LogonNotify


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::LogonNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">IWRdsProtocolConnection::LogonNotify</a>.]

Specifies that the user has logged on to the session.


## -parameters




### -param hClientToken [in]

A pointer to a user token handle.


### -param wszUserName [in]

A pointer to a string that contains the user name.


### -param wszDomainName [in]

A pointer to a string that contains the domain name for the user.


### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that contains the session ID associated with the user.


## -remarks



The Remote Desktop Services service also calls this method when  the state of the session has changed.

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a <a href="https://msdn.microsoft.com/e99a86ee-af0e-46db-8dad-69703ca84fa0">Remote Desktop Services API</a> being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

