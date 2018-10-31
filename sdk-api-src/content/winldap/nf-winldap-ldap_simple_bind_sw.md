---
UID: NF:winldap.ldap_simple_bind_sW
title: ldap_simple_bind_sW function
author: windows-sdk-content
description: The ldap_simple_bind_s function synchronously authenticates a client to a server, using a plaintext password.
old-location: ldap\ldap_simple_bind_s.htm
tech.root: ldap
ms.assetid: c3edca12-2dde-4f64-a479-2fbda8a4a996
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_ldap_ldap_simple_bind_s, ldap.ldap__simple__bind__s, ldap.ldap_simple_bind_s, ldap_simple_bind_s, ldap_simple_bind_s function [LDAP], ldap_simple_bind_sA, ldap_simple_bind_sW, winldap/ldap_simple_bind_s, winldap/ldap_simple_bind_sA, winldap/ldap_simple_bind_sW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_simple_bind_sW (Unicode) and ldap_simple_bind_sA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_simple_bind_s
 - ldap_simple_bind_sA
 - ldap_simple_bind_sW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_simple_bind_sW function


## -description


The <b>ldap_simple_bind_s</b> function synchronously authenticates a client to a server, using a plaintext password.
<div class="alert"><b>Caution</b>  This function sends the name and password without encrypting them, and an unauthorized user, on the network, could read the password. Unless a TLS (SSL) encrypted session has been established, do not this function. For more information about how to set up an encrypted session, see <a href="https://msdn.microsoft.com/218b4cf2-e582-4052-8206-35c2ba2fe302">Initializing a Session</a>.</div><div> </div>

## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

The name of the user to bind as. The bind operation uses the <i>dn</i> and <i>passwd</i> parameters to authenticate the user.


### -param passwd [in]

The password of the user specified in the <i>dn</i> parameter.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_simple_bind_s</b> function initiates a simple synchronous bind operation to authenticate a client to an LDAP server. Subsequent bind calls can be used to reauthenticate using the same connection.

Upon completion of the bind operation, <b>ldap_simple_bind_s</b> returns to the caller. Use 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> if you prefer to have the operation carried out asynchronously. Be aware that if an LDAP 2 server is contacted, do not attempt other operations over the connection until the bind call has completed successfully.

Multithreading: Bind calls are unsafe because they apply to the connection as a whole. Use caution if threads share connections, and try to thread binds with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, terminate the session by passing the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle to the  <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> function.  Also, if the <b>ldap_simple_bind_s</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.




## -see-also




<a href="https://msdn.microsoft.com/d11da030-b521-4469-9212-63800b412e68">Establishing an LDAP Session</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

