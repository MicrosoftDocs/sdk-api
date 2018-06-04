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

# cldap_openW function


## -description


The <b>cldap_open</b> function establishes a session with an LDAP server over a connectionless User Datagram Protocol (UDP) service. This is an alternate to using TCP/IP.


## -parameters




### -param HostName [in]

A pointer to a null-terminated string that contains a list of host names or dotted strings that represent the IP address of LDAP server hosts. Use a single space to separate the host names in the list. Each host name in the list may be followed by a port number. The optional port number is separated from the host itself with a colon (:). The LDAP run time attempts connection with the hosts in the order listed, stopping when a successful connection is made.


### -param PortNumber [in]

The port number to be used. If no port number is specified, the default is port 389, which is defined as LDAP_PORT. If  port numbers are included in the <i>HostName</i> parameter, this parameter is ignored.


## -returns



If the function succeeds, a session handle, in the form of a pointer to an LDAP structure is returned. Free the session handle with a call to <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> when it is no longer required.

If the function fails, the return value is <b>NULL</b>. To get the error code, call 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> or the Win32 function 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>cldap_open</b> function, unlike 
<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>, creates a connection block for UDP-based connectionless LDAP services. No TCP session is maintained. Like <b>ldap_open</b>, <b>cldap_open</b> allocates an LDAP structure to maintain state data for the session, and then attempts to make the connection before returning to the caller. The call returns a session handle, which you pass to subsequent LDAP function calls in the course of the session. When finished with the session, always free the allocated session handle by using <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>.

Using LDAP over UDP does not support binding and does not support TLS (SSL) or SASL.

Multithreading: Calls to <b>cldap_open</b> are thread-safe.

<div class="alert"><b>Note</b>  When using <b>cldap_open</b>, the connection is opened by an anonymous user.  The only available operations are those that an anonymous user can run.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a>



<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

