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

# ldap_stop_tls_s function


## -description


The <b>ldap_stop_tls_s</b> function stops the encryption operation started by a call to <a href="https://msdn.microsoft.com/faca9324-5a85-47b0-9d6a-c62ec3c1ee80">ldap_start_tls_s</a>.


## -parameters




### -param ExternalHandle [in]

A pointer to an <b>LDAP</b> structure that represents the current session.


## -returns



Returns <b>TRUE</b> if the function call succeeds. Returns <b>FALSE</b> if a bind is currently in progress on the connection, if the connection is not actively connected to the server, or if TLS (SSL) negotiation is in progress on the connection.




## -remarks



The <b>ldap_stop_tls_s</b> function should only be called on a connection for which TLS (SSL) was established by using <a href="https://msdn.microsoft.com/faca9324-5a85-47b0-9d6a-c62ec3c1ee80">ldap_start_tls_s</a>. It should not be called on a TLS (SSL) connection established by some other function, such as <a href="https://msdn.microsoft.com/04c13577-9d9f-4305-8aa2-fad81c03290a">ldap_sslinit</a>. Any outstanding requests on the connection will be abandoned before TLS encryption is terminated. If this function fails, that is, returns <b>FALSE</b>, close the connection by using <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> or <a href="https://msdn.microsoft.com/b4dcf3cc-d4cb-40ca-a57e-150d4008108c">ldap_unbind_s</a> because the connection can be left in an indeterminate state.




## -see-also




<a href="https://msdn.microsoft.com/10e97876-21ae-49d3-9cf7-890e95b0e93d">Using Start-stop TLS Encryption</a>



<a href="https://msdn.microsoft.com/faca9324-5a85-47b0-9d6a-c62ec3c1ee80">ldap_start_tls_s</a>
 

 

