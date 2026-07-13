---
UID: NF:winldap.ldap_bind_sW
title: ldap_bind_sW function (winldap.h)
description: The ldap_bind_sW (Unicode) function (winldap.h) synchronously authenticates a client to the LDAP server. 
helpviewer_keywords: ["_ldap_ldap_bind_s", "ldap.ldap__bind__s", "ldap.ldap_bind_s", "ldap_bind_s", "ldap_bind_s function [LDAP]", "ldap_bind_sW", "winldap/ldap_bind_s", "winldap/ldap_bind_sW"]
old-location: ldap\ldap_bind_s.htm
tech.root: ldap
ms.assetid: 67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_bind_s, ldap.ldap__bind__s, ldap.ldap_bind_s, ldap_bind_s, ldap_bind_s function [LDAP], ldap_bind_sA, ldap_bind_sW, winldap/ldap_bind_s, winldap/ldap_bind_sA, winldap/ldap_bind_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_bind_sW (Unicode) and ldap_bind_sA (ANSI)
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
 - ldap_bind_sW
 - winldap/ldap_bind_sW
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
 - ldap_bind_s
 - ldap_bind_sA
 - ldap_bind_sW
---

# ldap_bind_sW function


## -description

The  <b>ldap_bind_s</b> function synchronously  authenticates a client to the LDAP server.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

Pointer to a null-terminated string that contains the distinguished name of the entry used to bind. This can be a DN, a UPN, a WinNT style user name, or other name that the directory server will accept as an identifier.

### -param cred [in]

Pointer to a null-terminated string that contains the credentials with which to authenticate. Arbitrary credentials can be passed using this parameter. The format and content of the credentials depends on the setting of the <i>method</i> parameter. For more information, see Remarks.

### -param method [in]

Indicates the authentication method to use.  For more information and  a listing of valid asynchronous authentication methods, see the Remarks section. For more information and a description of the valid asynchronous authentication method, see 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The introduction of User Account Control in Windows Server 2008 and Windows Vista has a very important consequence with regard to making modifications or additions in LDAP.  When a user is logged on to a DC with a restricted UAC Administrator token and using <b>NULL</b> credentials, any modification or addition to the directory, or any schema change operation, will fail. This includes DirSync searches, retrieving the SACL from an object's <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor">ntSecurityDescriptor</a> attribute when using SecurityDescriptorFlags, and many other operations.

These will all fail with insufficient access rights.

If User Account Control is in effect when an administrator logs on to a DC, the administrator will get a restricted token in the logon session. If he or she then uses <b>ldap_bind_s</b> with <b>NULL</b> credentials, then operations that make modifications or additions will fail.

The implementation of <b>ldap_bind_s</b> supports the authentication methods listed in the following table. Calling <b>ldap_bind_s</b> with the LDAP_AUTH_SIMPLE option is equivalent to calling <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>.

<table>
<tr>
<th>Method</th>
<th>Description</th>
<th>Credential</th>
</tr>
<tr>
<td><b>LDAP_AUTH_SIMPLE</b></td>
<td>
Authentication with a plaintext password.

</td>
<td>
A string that contains the user password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_DIGEST</b></td>
<td>
Digest authentication package.

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_DPA</b></td>
<td>
Distributed password authentication. Used by Microsoft Membership System.

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_MSN</b></td>
<td>
Microsoft Network Authentication Service.

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_NEGOTIATE</b></td>
<td>
Generic security services (GSS) (Snego). Does not provide authentication, but instead chooses the most appropriate authentication method from a list of available services and passes all authentication data to that service.

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_NTLM</b></td>
<td>
NT LAN Manager

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_SICILY</b></td>
<td>
Covers package negotiation to MSN servers.

</td>
<td>
To log in as the current user, set the <i>dn</i> and <i>cred</i> parameters to <b>NULL</b>. To log in as another user, set the <i>dn</i> parameter to <b>NULL</b> and the <i>cred</i> parameter to  a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure with the appropriate user name, domain name, and password.

</td>
</tr>
<tr>
<td><b>LDAP_AUTH_SSPI</b></td>
<td>
Obsolete. Included for backward compatibility. Using this constant selects GSS (Snego) negotiation service.

</td>
<td>
Same as <b>LDAP_AUTH_NEGOTIATE</b>.

</td>
</tr>
</table>
 

For asynchronous bind authentication, use <b>LDAP_AUTH_SIMPLE</b> with <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>.

The bind operation identifies a client to the directory server by providing a distinguished name and some type of authentication credential, such as a password. The exact credentials are dependent on the authentication method used. If you pass in <b>NULL</b> for the credentials with <b>ldap_bind_s()</b> (non-simple), the current user or service credentials will be used. If a simple bind method (as in 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>) is specified, it is equivalent to a <b>NULL</b> plaintext password. For more information, see 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>.

Be aware that LDAP 2 servers require an application to bind before attempting other operations that require authentication.

Multithreading: Bind calls are unsafe because they apply to the connection as a whole. Use caution if threads share connections and try to thread the bind operations with other operations.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>.</div>
<div> </div>
When all of the operations on the session handle are completed, the session must be terminated by passing the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle to the  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> function.  Also, if the <b>ldap_bind_s</b> call fails, the session handle should be freed with a call to  <b>ldap_unbind</b> when no longer required for error recovery.





> [!NOTE]
> The winldap.h header defines ldap_bind_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
