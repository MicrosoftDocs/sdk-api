---
UID: NC:ntsecpkg.LSA_AP_LOGON_USER_EX
title: LSA_AP_LOGON_USER_EX (ntsecpkg.h)
description: Authenticates a user's logon credentials.
helpviewer_keywords: ["LSA_AP_LOGON_USER_EX","LSA_AP_LOGON_USER_EX callback","LsaApLogonUserEx","LsaApLogonUserEx callback function [Security]","STATUS_ACCOUNT_DISABLED","STATUS_INVALID_LOGON_HOURS","STATUS_INVALID_WORKSTATION","STATUS_PASSWORD_EXPIRED","_lsa_lsaaplogonuserex","ntsecpkg/LsaApLogonUserEx","security.lsaaplogonuserex"]
old-location: security\lsaaplogonuserex.htm
tech.root: security
ms.assetid: 7778292a-7062-4f49-b4a9-6784e5e4ccd7
ms.date: 12/05/2018
ms.keywords: LSA_AP_LOGON_USER_EX, LSA_AP_LOGON_USER_EX callback, LsaApLogonUserEx, LsaApLogonUserEx callback function [Security], STATUS_ACCOUNT_DISABLED, STATUS_INVALID_LOGON_HOURS, STATUS_INVALID_WORKSTATION, STATUS_PASSWORD_EXPIRED, _lsa_lsaaplogonuserex, ntsecpkg/LsaApLogonUserEx, security.lsaaplogonuserex
f1_keywords:
- ntsecpkg/LsaApLogonUserEx
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- LsaApLogonUserEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_AP_LOGON_USER_EX callback function


## -description


Authenticates a user's logon credentials.

 This function is called by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) only for a user's initial logon. Subsequent authentication requests must use 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>. If <b>LsaApLogonUserEx</b> succeeds, it creates a logon session and returns information used to build the token representing the newly logged on user.

This function differs from 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a> in that the machine name is added to the audit record for the logon attempt.


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data type representing the LSA client's request.


### -param LogonType [in]

A 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> structure which identifies the type of logon being attempted.


### -param AuthenticationInformation [in]

Supplies the authentication information specific to the authentication package. The LSA will free this buffer.


### -param ClientAuthenticationBase [in]

Provides the address of the authentication information within the client process. This may be necessary to remap any pointers within the <i>AuthenticationInformation</i> buffer.


### -param AuthenticationInformationLength [in]

Indicates the length of the <i>AuthenticationInformation</i> buffer.


### -param *ProfileBuffer [out]

Pointer that receives the address of the profile buffer in the client process. The authentication package is responsible for allocating the <i>ProfileBuffer</i> buffer within the client process by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function. However, if the LSA subsequently encounters an error which prevents a successful logon, then the LSA will take care of freeing this buffer. 




The contents of this buffer are determined by the authentication package. The LSA does not alter this buffer; it simply returns the value to the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.


### -param ProfileBufferLength [out]

Pointer to a <b>ULONG</b> that receives the length of the <i>ProfileBuffer</i> buffer, in bytes.


### -param LogonId [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> variable that receives the new logon ID that uniquely identifies this logon session. The authentication package is responsible for allocating this <b>LUID</b> and creating the LSA logon session for this logon.


### -param SubStatus [out]

Pointer to an NTSTATUS that receives the reason for failures due to account restrictions. The values returned in <i>SubStatus</i> are determined by the authentication package. 




The following are <i>SubStatus</i> values for the MSV1_0 and Kerberos authentication packages.

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
The user account has time restrictions and cannot be used to log on at this time.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_INVALID_WORKSTATION"></a><a id="status_invalid_workstation"></a><dl>
<dt><b>STATUS_INVALID_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The user account has workstation restrictions and cannot be used to log on from the current workstation.

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


### -param TokenInformationType [out]

Pointer that receives the address of an 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ne-ntsecpkg-lsa_token_information_type">LSA_TOKEN_INFORMATION_TYPE</a> value that indicates the type of information returned for inclusion in the token to be created. The information is returned by means of the <i>TokenInformation</i> parameter.


### -param *TokenInformation [out]

Pointer that receives the address of information to be included in the token. The format and content of <i>TokenInformation</i> are indicated by the <i>TokenInformationType</i> parameter. Your authentication package is responsible for allocating the memory used by <i>TokenInformation</i>; however, this memory will be freed by the LSA.


### -param *AccountName [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that receives the name of the user account. <i>AccountName</i> must always be returned regardless of the success or failure of the call; its string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AccountName</i> It will be freed by the LSA.


### -param *AuthenticatingAuthority [out]

Optional. Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that receives the description of the authenticating authority for the logon. This parameter may be <b>NULL</b>. This string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AuthenticatingAuthority</i>; however, this memory will be freed by the LSA. 




The MSV1_0 authentication package returns the domain name of the domain validating the account. The Kerberos authentication package returns the NetBIOS domain name.


### -param *MachineName [out]

Optional. Pointer that receives the address of an <a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure containing the name of the client's workstation. This information is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>MachineName</i>; however, this memory will be freed by the LSA. 




The MSV1_0 authentication package returns the NetBIOS name of the client's workstation.


## -returns



If the function succeeds, it should return STATUS_SUCCESS.

Otherwise, it should return an NTSTATUS error code, which can be one of the following values or one of the 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
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
The user account and password are legitimate, but user account restrictions prevent successful logon at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_VALIDATION_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The authentication information provided is recognized by the authentication package.

</td>
</tr>
</table>
 

Calling applications can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



Authentication packages must implement one of the following functions: 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>, <b>LsaApLogonUserEx</b>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a>.

<b>LsaApLogonUserEx</b> was added for C2 certification. C2 is a security classification defined by the United States government.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ne-ntsecpkg-lsa_token_information_type">LSA_TOKEN_INFORMATION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>
 

 

