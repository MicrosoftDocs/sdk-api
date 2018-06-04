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

# ldap_connect function


## -description


The <b>ldap_connect</b> function establishes a connection with the server.


## -parameters




### -param ld [in]

The session handle obtained from <a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>.


### -param timeout [in]

A pointer to an <a href="https://msdn.microsoft.com/8e551e7c-7237-4761-92e8-c352c3adda77">LDAP_TIMEVAL</a> structure that specifies the number of seconds to spend in an attempt to establish a connection before a timeout. If <b>NULL</b>, the function uses a default timeout value.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Although it is not required that a client call <b>ldap_connect</b> to establish a connection to the server, it is good programming practice to do so. If the connection does not exist, other functions, for example,  <a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a>, perform the call internally. However, if you have to troubleshoot this part of your application, establishing the connection prior to making the call to some other function, for example <b>ldap_bind_s</b>, will also separate the possible problems if the connection fails. Alternately,  you can specify additional options on the connection block. For example, a client can call 
<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a> to initialize a session, then call 
<b>ldap_connect</b>, with a non-<b>NULL</b> timeout parameter value, to connect to the server with a specified time-out.

If the call to <b>ldap_connect</b> succeeds, the client is connected to the LDAP server as an  anonymous user. The session handle should be freed with a call to <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> when it is no longer required.

If the <b>ldap_connect</b> call fails, the session handle should be freed with a call to  <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> when no longer required for error recovery.




## -see-also




<a href="https://msdn.microsoft.com/d11da030-b521-4469-9212-63800b412e68">Establishing an LDAP Session</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/8e551e7c-7237-4761-92e8-c352c3adda77">LDAP_TIMEVAL</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

