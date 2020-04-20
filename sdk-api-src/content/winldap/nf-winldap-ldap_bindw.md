---
UID: NF:winldap.ldap_bindW
title: ldap_bindW function (winldap.h)
description: Asynchronously authenticates a client with the LDAP server.helpviewer_keywords: ["_ldap_ldap_bind","ldap.ldap__bind","ldap.ldap_bind","ldap_bind","ldap_bind function [LDAP]","ldap_bindA","ldap_bindW","winldap/ldap_bind","winldap/ldap_bindA","winldap/ldap_bindW"]
old-location: ldap\ldap_bind.htm
tech.root: ldap
ms.assetid: 889636f2-3dd0-4027-aa35-d7b7930d9e69
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_bind, ldap.ldap__bind, ldap.ldap_bind, ldap_bind, ldap_bind function [LDAP], ldap_bindA, ldap_bindW, winldap/ldap_bind, winldap/ldap_bindA, winldap/ldap_bindW
f1_keywords:
- winldap/ldap_bind
dev_langs:
- c++
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_bindW (Unicode) and ldap_bindA (ANSI)
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
- ldap_bind
- ldap_bindA
- ldap_bindW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_bindW function


## -description


The <b>ldap_bind</b> function asynchronously authenticates a client with the LDAP server. The bind operation identifies a client to the directory server by providing a distinguished name and some type of authentication credential, such as a password. The authentication method  used determines the type of required credential.
<div class="alert"><b>Caution</b>  Unless a TLS (SSL) encrypted session is established, do not use this function. This function sends the name and password in plaintext. An unauthorized user, monitoring network traffic, could read the password. For more information about how to establish an encrypted session, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/initializing-a-session">Initializing a Session</a>.</div><div> </div>

## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry used to bind.


### -param cred [in]

A pointer to a null-terminated string that contains the credentials to use for authentication. Arbitrary credentials can be passed using this parameter. The format and content of the credentials depend on the setting of the method parameter. For more information, see the Remarks section.


### -param method [in]

The authentication method to use.


## -returns



If the function succeeds, the return value is the message ID of the initiated operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP structure.




## -remarks



This implementation of <b>ldap_bind</b> supports the following authentication method.

<table>
<tr>
<th>Authentication method</th>
<th>Description</th>
<th>Credential</th>
</tr>
<tr>
<td><b>LDAP_AUTH_SIMPLE</b></td>
<td>Authentication with a plaintext password.</td>
<td>A string that contains the user password.</td>
</tr>
</table>
 

<b>LDAP_AUTH_SIMPLE</b> is the only authentication method compatible with the asynchronous version of binding; <b>ldap_bind</b>. Using any other authentication method with <b>ldap_bind</b> will fail and return <b>LDAP_PARAM_ERROR</b>. Calling <b>ldap_bind</b> with the <b>LDAP_AUTH_SIMPLE</b> method is equivalent to calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>. All other authentication methods require synchronous binding as provided by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>.

Be aware that LDAP 2 servers require an application to bind before attempting any other operations that require authentication.

Multithreading: Bind calls are not safe because they apply to the connection as a whole. Use caution if threads share connections and, when possible, thread the bind operations with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified by using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, terminate the session by passing the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle to the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> function.  Also, if the <b>ldap_bind</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
 

 

