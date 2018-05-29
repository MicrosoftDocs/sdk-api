---
UID: NF:winldap.ldap_simple_bindA
title: ldap_simple_bindA function
author: windows-sdk-content
description: asynchronously authenticates a client to a server, using a plaintext password.
old-location: ldap\ldap_simple_bind.htm
old-project: LDAP
ms.assetid: 13fc47c5-094b-4a91-8e5f-bfff8c72b431
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_simple_bind, ldap.ldap__simple__bind, ldap.ldap_simple_bind, ldap_simple_bind, ldap_simple_bind function [LDAP], ldap_simple_bindA, ldap_simple_bindW, winldap/ldap_simple_bind, winldap/ldap_simple_bindA, winldap/ldap_simple_bindW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_simple_bindW (Unicode) and ldap_simple_bindA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_simple_bind
-	ldap_simple_bindA
-	ldap_simple_bindW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_simple_bindA function


## -description


The <b>ldap_simple_bind</b> function
    asynchronously authenticates a client to a server, using a plaintext password.
<div class="alert"><b>Caution</b>  This function sends the name and password without encrypting them, and therefore someone eavesdropping on the network could read the password. Unless a TLS (SSL) encrypted session has been established, do not use this function. For more information about how to set up an encrypted session, see <a href="https://msdn.microsoft.com/218b4cf2-e582-4052-8206-35c2ba2fe302">Initializing a Session</a>.</div><div> </div>

## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

The name of the user to bind as. The bind operation uses the <i>dn</i> and <i>passwd</i> parameters to authenticate the user.


### -param passwd [in]

The password of the user specified in the <i>dn</i> parameter.


## -returns



If the function succeeds, it returns the message ID of the operation initiated.

If the function fails, it returns -1 and sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_simple_bind</b> function initiates a simple asynchronous bind operation to authenticate a client to an LDAP server. Subsequent bind calls can be used to reauthenticate using the same connection.

To authenticate as a specific user, provide both the name of the entry (user) and the password for that entry. To authenticate an anonymous user, when no access permissions are required, pass <b>NULL</b> to both the <i>dn</i> and <i>passwd</i> parameters.

As an asynchronous function, <b>ldap_simple_bind</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous bind operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>. Be aware that if an LDAP 2 server is contacted, do not attempt other operations over the connection until the bind call has successfully completed.

To return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/c3edca12-2dde-4f64-a479-2fbda8a4a996">ldap_simple_bind_s</a>.

Multithreading: Bind calls are not safe because they apply to the connection as a whole. Use caution if threads share connections and try to thread binds with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, terminate the session by passing the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle to the  <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> function.  Also, if the <b>ldap_simple_bind</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.

The <b>ldap_simple_bind</b> function is designed to bind to the local domain. The function cannot be used for cross forest authentication.




## -see-also




<a href="https://msdn.microsoft.com/d11da030-b521-4469-9212-63800b412e68">Establishing an LDAP Session</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/c3edca12-2dde-4f64-a479-2fbda8a4a996">ldap_simple_bind_s</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

