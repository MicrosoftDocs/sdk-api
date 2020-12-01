---
UID: NF:subauth.Msv1_0SubAuthenticationFilter
title: Msv1_0SubAuthenticationFilter function (subauth.h)
description: Performs user logon authentication that is specific to domain controllers.
helpviewer_keywords: ["LOGON_GUEST","LOGON_NOENCRYPTION","MSV1_0_GUEST_LOGON","MSV1_0_PASSTHRU","Msv1_0SubAuthenticationFilter","Msv1_0SubAuthenticationFilter function [Security]","USER_ALL_PARAMETERS","_lsa_msv1_0subauthenticationfilter","security.msv1_0subauthenticationfilter","subauth/Msv1_0SubAuthenticationFilter"]
old-location: security\msv1_0subauthenticationfilter.htm
tech.root: security
ms.assetid: d7162830-8cab-4ec1-afcb-7892f5e435d3
ms.date: 12/05/2018
ms.keywords: LOGON_GUEST, LOGON_NOENCRYPTION, MSV1_0_GUEST_LOGON, MSV1_0_PASSTHRU, Msv1_0SubAuthenticationFilter, Msv1_0SubAuthenticationFilter function [Security], USER_ALL_PARAMETERS, _lsa_msv1_0subauthenticationfilter, security.msv1_0subauthenticationfilter, subauth/Msv1_0SubAuthenticationFilter
req.header: subauth.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Msv1_0SubAuthenticationFilter
 - subauth/Msv1_0SubAuthenticationFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Subauth.h
api_name:
 - Msv1_0SubAuthenticationFilter
---

# Msv1_0SubAuthenticationFilter function


## -description

The <b>Msv1_0SubAuthenticationFilter</b> function performs user logon authentication that is specific to domain controllers.

The function receives the user's logon data and all information found for the user in the domain controller's <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) database.

This function is implemented by custom subauthentication package DLLs for use with the Kerberos and MSV1_0 authentication packages.

## -parameters

### -param LogonLevel [in]

Specifies the level of information given in <i>LogonInformation</i>. This parameter is normally set to NetlogonInteractiveInformation.

### -param LogonInformation [in]

A pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-netlogon_logon_identity_info">NETLOGON_LOGON_IDENTITY_INFO</a> structure. Members of this structure contain information about the user who is logging on. The <b>LogonDomainName</b> member is ignored.

### -param Flags [in]

Optional. Contains flags that describe the circumstances of the logon. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_PASSTHRU"></a><a id="msv1_0_passthru"></a><dl>
<dt><b>MSV1_0_PASSTHRU</b></dt>
</dl>
</td>
<td width="60%">
Pass-through authentication. The user is not connecting to this machine.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_GUEST_LOGON"></a><a id="msv1_0_guest_logon"></a><dl>
<dt><b>MSV1_0_GUEST_LOGON</b></dt>
</dl>
</td>
<td width="60%">
This is a retry of the logon using the Guest account.

</td>
</tr>
</table>

### -param UserAll [in]

A pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-user_all_information">USER_ALL_INFORMATION</a> structure that contains the description of the user as returned from the SAM database.

### -param WhichFields [out]

Returns the members of the <a href="/windows/desktop/api/subauth/ns-subauth-user_all_information">USER_ALL_INFORMATION</a> structure that need to be written back to the SAM database. These members will be written only if <b>Msv1_0SubAuthenticationFilter</b> returns success. Only the following value is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USER_ALL_PARAMETERS"></a><a id="user_all_parameters"></a><dl>
<dt><b>USER_ALL_PARAMETERS</b></dt>
</dl>
</td>
<td width="60%">
Write the data contained in the <b>Parameters</b> member of the <i>UserAll</i> structure back to the SAM database.

If the size of the <b>Parameters</b> member's <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> buffer is changed, <b>Msv1_0SubAuthenticationFilter</b> must delete the buffer by using the <a href="/windows/desktop/Midl/midl-user-free-1">MIDL_user_free</a> function and reallocate it by using the <a href="https://msdn.microsoft.com/">MIDL_user_allocate</a> function.

</td>
</tr>
</table>

### -param UserFlags [out]

Values to be returned from the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function in that function's <i>ProfileBuffer</i> parameter. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_GUEST"></a><a id="logon_guest"></a><dl>
<dt><b>LOGON_GUEST</b></dt>
</dl>
</td>
<td width="60%">
This was a guest logon.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_NOENCRYPTION"></a><a id="logon_noencryption"></a><dl>
<dt><b>LOGON_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The caller did not specify encrypted credentials.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  By convention, subauthentication packages return bits only in the high order byte of the <i>UserFlags</i> parameter.</div>
<div> </div>

### -param Authoritative [out]

A pointer to a Boolean value that indicates whether the status returned is an authoritative status that should be returned to the original caller. If the value returned is <b>FALSE</b>, the logon request can be tried again on another domain controller. This parameter should return valid information regardless of the return value of the function call. This parameter is not used with the Kerberos authentication package.

### -param LogoffTime [out]

A pointer to a value that receives the time at which the user should log off the system. This time is used to control the logon lifetime and is specified as a GMT-relative Windows system time.

### -param KickoffTime [out]

A pointer to a value that receives the time at which the user should be logged off the system. This time is used to control the logon lifetime and is specified as a GMT-relative system time. If the user is not to be automatically logged off, specify a large positive value, as follows:


```cpp
KickoffTime->HighPart = 0x7FFFFFFF;
KickoffTime->LowPart = 0xFFFFFFFF;

```

## -returns

This function must return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
There was no error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The account is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The account has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_LOCKED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The account is locked out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
<i>LogonLevel</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_LOGON_HOURS</b></dt>
</dl>
</td>
<td width="60%">
The user is not authorized to log on at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The user is not authorized to log on to the specified workstation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The specified user has no account.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PASSWORD_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The password is expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PASSWORD_MUST_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The password must change on next logon.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_WRONG_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The password was not valid.

</td>
</tr>
</table>
 

When the <b>Msv1_0SubAuthenticationFilter</b> function is used with the Kerberos authentication package, if the function call returns STATUS_SUCCESS and one of the two parameters <i>LogoffTime</i> or <i>KickoffTime</i> has a nonzero value, this value is used as the ticket lifetime. If, on the other hand, the values of both parameters are nonzero, the smaller of these two values is used.

If the value that is used for the ticket lifetime (the sooner of <i>LogoffTime</i> and <i>KickoffTime</i>) is greater than the default ticket lifetime, then that value will be used as the maximum renewal time for the ticket. Conversely, if the larger of the two values (the later of <i>LogoffTime</i> and <i>KickoffTime</i>) is less than the default ticket lifetime, this value will be used as the ticket lifetime. For more information, see 
<a href="/windows/desktop/SecAuthN/microsoft-kerberos">Microsoft Kerberos</a>.

When used with the Kerberos authentication package, if this function returns an error, the <a href="/windows/desktop/SecGloss/k-gly">Key Distribution Center</a> (KDC) will return the Kerberos error KDC_ERR_POLICY, with the status value as the extended error code.

## -remarks

Implementations of this function should not execute any operations that cause <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> (LDAP) traffic. For example, do not connect to and query the <a href="/windows/desktop/AD/active-directory-domain-services">Active Directory</a> database.

After the MSV1_0 or Kerberos authentication package has validated a logon, the <b>Msv1_0SubAuthenticationFilter</b> function can perform additional validation to determine whether a user can log on to a network account. This function is called if the subauthentication package DLL is properly registered as 'Auth0' in the domain controller's registry. The registry path is different depending on whether the function is in a MSV1_0 or Kerberos Subauthentication package DLL. 

This filter routine may return STATUS_SUCCESS, which indicates that the logon should proceed, or a failure code, which indicates that the additional validation failed.