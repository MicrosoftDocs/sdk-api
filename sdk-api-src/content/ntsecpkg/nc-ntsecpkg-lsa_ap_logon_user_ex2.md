---
UID: NC:ntsecpkg.LSA_AP_LOGON_USER_EX2
title: LSA_AP_LOGON_USER_EX2 (ntsecpkg.h)
description: Used to authenticate a user logon attempt on the user's initial logon. A new logon session is established for the user, and validation information for the user is returned.
helpviewer_keywords: ["LSA_AP_LOGON_USER_EX2","LSA_AP_LOGON_USER_EX2 callback","LsaApLogonUserEx2","LsaApLogonUserEx2 callback function [Security]","STATUS_ACCOUNT_DISABLED","STATUS_INVALID_LOGON_HOURS","STATUS_INVALID_WORKSTATION","STATUS_PASSWORD_EXPIRED","_lsa_lsaaplogonuserex2","ntsecpkg/LsaApLogonUserEx2","security.lsaaplogonuserex2"]
old-location: security\lsaaplogonuserex2.htm
tech.root: security
ms.assetid: 002ac773-bd46-49b5-b54c-6b8f5d5ef9f7
ms.date: 12/05/2018
ms.keywords: LSA_AP_LOGON_USER_EX2, LSA_AP_LOGON_USER_EX2 callback, LsaApLogonUserEx2, LsaApLogonUserEx2 callback function [Security], STATUS_ACCOUNT_DISABLED, STATUS_INVALID_LOGON_HOURS, STATUS_INVALID_WORKSTATION, STATUS_PASSWORD_EXPIRED, _lsa_lsaaplogonuserex2, ntsecpkg/LsaApLogonUserEx2, security.lsaaplogonuserex2
req.header: ntsecpkg.h
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
 - LSA_AP_LOGON_USER_EX2
 - ntsecpkg/LSA_AP_LOGON_USER_EX2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - LsaApLogonUserEx2
---

# LSA_AP_LOGON_USER_EX2 callback function


## -description

Used to authenticate a user logon attempt on the user's initial logon.
			A new logon session is established for the user, and validation information for the user is returned.

## -parameters

### -param ClientRequest [in]

Pointer to a 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> opaque buffer representing the client's request.

### -param LogonType [in]

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value that identifies the type of logon.

### -param ProtocolSubmitBuffer [in]

Buffer that supplies the authentication information specific to the authentication package.

### -param ClientBufferBase [in]

Buffer that provides the address within the client process at which the authentication information was resident. This might be necessary to fix any pointers within the authentication information buffer.

### -param SubmitBufferSize [in]

A <b>ULONG</b> value that indicates the size, in bytes, of the authentication information buffer.

### -param ProfileBuffer [out]

Pointer that receives the address of the profile buffer in the client process. The authentication package is responsible for allocating <i>ProfileBuffer</i> within the client process by calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function. However, if the LSA subsequently encounters an error which prevents a successful logon, then the LSA will take care of freeing this buffer. 




The contents of this buffer are determined by the authentication package. The LSA does not alter this buffer; it simply returns the value to the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.

### -param ProfileBufferSize [out]

Pointer to a <b>ULONG</b> that receives the size of the <i>ProfileBuffer</i> buffer.

### -param LogonId [out]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> variable that receives the new logon ID that uniquely identifies this logon session. The authentication package is responsible for allocating this <b>LUID</b> and creating the LSA logon session for this logon.

### -param SubStatus [out]

Pointer to an NTSTATUS that receives the reason for failures due to account restrictions. The values returned in <i>SubStatus</i> are determined by the authentication package. 




The following table lists the <i>SubStatus</i> values for the MSV1_0 and Kerberos authentication packages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATUS_INVALID_LOGON_HOURS"></a><a id="status_invalid_logon_hours"></a><dl>
<dt><b>STATUS_INVALID_LOGON_HOURS</b></dt>
</dl>
</td>
<td width="60%">
The user account has time restrictions; it cannot be used to log on at this time.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_INVALID_WORKSTATION"></a><a id="status_invalid_workstation"></a><dl>
<dt><b>STATUS_INVALID_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The user account has workstation restrictions; it cannot be used to log on to the current workstation.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_PASSWORD_EXPIRED"></a><a id="status_password_expired"></a><dl>
<dt><b>STATUS_PASSWORD_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The user account password has expired.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_ACCOUNT_DISABLED"></a><a id="status_account_disabled"></a><dl>
<dt><b>STATUS_ACCOUNT_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The user account is currently disabled and cannot be used to log on.

</td>
</tr>
</table>
 

More information about NTSTATUS codes can be found in the Subauth.h header file shipped with the Platform SDK.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

### -param TokenInformationType [out]

Pointer that receives the address of an 
<a href="/windows/desktop/api/ntsecpkg/ne-ntsecpkg-lsa_token_information_type">LSA_TOKEN_INFORMATION_TYPE</a> value that indicates the type of information returned for inclusion in the token to be created. The information is returned by means of the <i>TokenInformation</i> parameter.

### -param TokenInformation [out]

Pointer that receives the address of information to be included in the token. The format and content of <i>TokenInformation</i> are indicated by the <i>TokenInformationType</i> parameter. Your authentication package is responsible for allocating the memory used by <i>TokenInformation</i>; however, this memory will be freed by the LSA.

### -param AccountName [out]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that receives the name of the user account. <i>AccountName</i> must always be returned regardless of the success or failure of the call; its string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AccountName</i>; however, this memory will be freed by the LSA.

### -param AuthenticatingAuthority [out]

Optional. Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that receives the description of the authenticating authority for the logon. This parameter may be <b>NULL</b>. This string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AuthenticatingAuthority</i>; however, this memory will be freed by the LSA. 




The MSV1_0 authentication package returns the domain name of the domain validating the account. The Kerberos authentication package returns the NetBIOS domain name.

### -param MachineName [out]

Optional. Pointer that receives the address of a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure containing the name of the client's computer. This string may optionally be omitted. This string is included in the audit record for this authentication attempt. Your authentication package is responsible for allocating the memory used by <i>MachineName</i>; however, this memory will be freed by the LSA. 




The MSV1_0 authentication package returns the NetBIOS name of the client's workstation.

### -param PrimaryCredentials [out]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a> structure that returns primary credentials for handing to other packages.

### -param SupplementalCredentials [out]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred_array">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> array of supplemental credentials for other packages.

## -returns

If the function succeeds, it should return STATUS_SUCCESS.

Otherwise, it should return an NTSTATUS error code, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The logon could not be completed because the client's memory quota is insufficient to allocate the return buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_LOGON_SERVERS</b></dt>
</dl>
</td>
<td width="60%">
No domain controllers are available to service the authentication request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOGON_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The logon attempt failed. The reason for failure is not specified; typical reasons include misspelled user names and passwords.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_RESTRICTION</b></dt>
</dl>
</td>
<td width="60%">
The user account and password were legitimate, but user account restrictions preventing successful logon at this time. For additional information see the <i>SubStatus</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_VALIDATION_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The authentication information provided is not recognized by the authentication package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_LOGON_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>LogonType</i> was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOGON_SESSION_COLLISION</b></dt>
</dl>
</td>
<td width="60%">
The logon ID selected for this logon session (in the <i>LogonId</i> parameter) already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NETLOGON_NOT_STARTED</b></dt>
</dl>
</td>
<td width="60%">
The SAM database or Netlogon service is required, but is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The client's virtual memory or pagefile quotas are insufficient to allocate the return buffer.

</td>
</tr>
</table>
 

Calling applications can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

Authentication packages must implement one of the following functions: 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>, 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex">LsaApLogonUserEx</a>, or <b>LsaApLogonUserEx2</b>.

## -see-also

<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a>



<a href="/windows/desktop/api/ntsecpkg/ne-ntsecpkg-lsa_token_information_type">LSA_TOKEN_INFORMATION_TYPE</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex">LsaApLogonUserEx</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>
