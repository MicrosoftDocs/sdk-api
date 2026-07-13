---
UID: NF:winldap.ldap_simple_bind_sW
title: ldap_simple_bind_sW function (winldap.h)
description: The ldap_simple_bind_sW (Unicode) function (winldap.h) synchronously authenticates a client to a server, using a plaintext password.
helpviewer_keywords: ["_ldap_ldap_simple_bind_s", "ldap.ldap__simple__bind__s", "ldap.ldap_simple_bind_s", "ldap_simple_bind_s", "ldap_simple_bind_s function [LDAP]", "ldap_simple_bind_sW", "winldap/ldap_simple_bind_s", "winldap/ldap_simple_bind_sW"]
old-location: ldap\ldap_simple_bind_s.htm
tech.root: ldap
ms.assetid: c3edca12-2dde-4f64-a479-2fbda8a4a996
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_simple_bind_s, ldap.ldap__simple__bind__s, ldap.ldap_simple_bind_s, ldap_simple_bind_s, ldap_simple_bind_s function [LDAP], ldap_simple_bind_sA, ldap_simple_bind_sW, winldap/ldap_simple_bind_s, winldap/ldap_simple_bind_sA, winldap/ldap_simple_bind_sW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_simple_bind_sW
 - winldap/ldap_simple_bind_sW
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
 - ldap_simple_bind_s
 - ldap_simple_bind_sA
 - ldap_simple_bind_sW
---

# ldap_simple_bind_sW function


## -description

The <b>ldap_simple_bind_s</b> function synchronously authenticates a client to a server, using a plaintext password.
<div class="alert"><b>Caution</b>  This function sends the name and password without encrypting them, and an unauthorized user, on the network, could read the password. Unless a TLS (SSL) encrypted session has been established, do not this function. For more information about how to set up an encrypted session, see <a href="/previous-versions/windows/desktop/ldap/initializing-a-session">Initializing a Session</a>.</div><div> </div>

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
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_simple_bind_s</b> function initiates a simple synchronous bind operation to authenticate a client to an LDAP server. Subsequent bind calls can be used to reauthenticate using the same connection.

Upon completion of the bind operation, <b>ldap_simple_bind_s</b> returns to the caller. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> if you prefer to have the operation carried out asynchronously. Be aware that if an LDAP 2 server is contacted, do not attempt other operations over the connection until the bind call has completed successfully.

Multithreading: Bind calls are unsafe because they apply to the connection as a whole. Use caution if threads share connections, and try to thread binds with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, terminate the session by passing the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle to the  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> function.  Also, if the <b>ldap_simple_bind_s</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.





> [!NOTE]
> The winldap.h header defines ldap_simple_bind_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
