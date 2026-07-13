---
UID: NF:winldap.ldap_simple_bindW
title: ldap_simple_bindW function (winldap.h)
description: The ldap_simple_bindW (Unicode) function (winldap.h) asynchronously authenticates a client to a server, using a plaintext password. 
helpviewer_keywords: ["_ldap_ldap_simple_bind", "ldap.ldap__simple__bind", "ldap.ldap_simple_bind", "ldap_simple_bind", "ldap_simple_bind function [LDAP]", "ldap_simple_bindW", "winldap/ldap_simple_bind", "winldap/ldap_simple_bindW"]
old-location: ldap\ldap_simple_bind.htm
tech.root: ldap
ms.assetid: 13fc47c5-094b-4a91-8e5f-bfff8c72b431
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_simple_bind, ldap.ldap__simple__bind, ldap.ldap_simple_bind, ldap_simple_bind, ldap_simple_bind function [LDAP], ldap_simple_bindA, ldap_simple_bindW, winldap/ldap_simple_bind, winldap/ldap_simple_bindA, winldap/ldap_simple_bindW
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
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_simple_bindW
 - winldap/ldap_simple_bindW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_simple_bind
 - ldap_simple_bindA
 - ldap_simple_bindW
---

# ldap_simple_bindW function


## -description

The <b>ldap_simple_bind</b> functionasynchronously authenticates a client to a server, using a plaintext password.
<div class="alert"><b>Caution</b>  This function sends the name and password without encrypting them, and therefore someone eavesdropping on the network could read the password. Unless a TLS (SSL) encrypted session has been established, do not use this function. For more information about how to set up an encrypted session, see <a href="/previous-versions/windows/desktop/ldap/initializing-a-session">Initializing a Session</a>.</div><div> </div>

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
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous bind operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>. Be aware that if an LDAP 2 server is contacted, do not attempt other operations over the connection until the bind call has successfully completed.

To return the results directly, use the synchronous routine 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>.

Multithreading: Bind calls are not safe because they apply to the connection as a whole. Use caution if threads share connections and try to thread binds with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, terminate the session by passing the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle to the  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> function.  Also, if the <b>ldap_simple_bind</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.

The <b>ldap_simple_bind</b> function is designed to bind to the local domain. The function cannot be used for cross forest authentication.





> [!NOTE]
> The winldap.h header defines ldap_simple_bind as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
