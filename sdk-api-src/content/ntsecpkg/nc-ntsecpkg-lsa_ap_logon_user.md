---
UID: NC:ntsecpkg.LSA_AP_LOGON_USER
title: LSA_AP_LOGON_USER
author: windows-driver-content
description: Authenticates a user's logon credentials.
old-location: security\lsaaplogonuser.htm
old-project: SecAuthN
ms.assetid: 4c8def77-d536-486e-a830-9df3848fbccb
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: LSA_AP_LOGON_USER, LsaApLogonUser, LsaApLogonUser function [Security], STATUS_ACCOUNT_DISABLED, STATUS_INVALID_LOGON_HOURS, STATUS_INVALID_WORKSTATION, STATUS_PASSWORD_EXPIRED, _lsa_lsaaplogonuser, ntsecpkg/LsaApLogonUser, security.lsaaplogonuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	LsaApLogonUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# LSA_AP_LOGON_USER callback


## -description


Authenticates a user's logon credentials.

This function is called only for a user's initial logon. Subsequent authentication requests must use 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.

If <b>LsaApLogonUser</b> succeeds, it creates a logon session. It also returns information used to build the token representing the newly logged-on user.


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> buffer that represents the LSA client's request. Your authentication package can pass this value into 
<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> and 
<a href="https://msdn.microsoft.com/c3a92039-7fb1-49e9-8e7a-0c902770543e">FreeClientBuffer</a> in order to identify the client process in which memory should be allocated or freed.


### -param LogonType [in]

A 
<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> value identifying the type of logon requested.


### -param AuthenticationInformation [in]

Supplies the authentication information specific to the authentication package. The LSA will free this buffer. This is the same input buffer passed into 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


### -param ClientAuthenticationBase [in]

Provides the address of the authentication information within the client process. This may be necessary to remap any pointers within the <i>AuthenticationInformation</i> buffer.


### -param AuthenticationInformationLength [in]

Indicates the length, in bytes, of the <i>AuthenticationInformation</i> buffer.


### -param *ProfileBuffer [out]

Pointer that receives the address of the profile buffer in the client process. The authentication package is responsible for allocating the <i>ProfileBuffer</i> buffer within the client process by calling the 
<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function. However, if the LSA subsequently encounters an error that prevents a successful logon, the LSA will free this buffer. 




The contents of this buffer are determined by the authentication package. The LSA does not alter this buffer; it simply returns the value to the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.


### -param ProfileBufferLength [out]

Pointer to a <b>ULONG</b> that receives the length of the <i>ProfileBuffer</i> buffer, in bytes.


### -param LogonId [out]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> that receives the new logon ID that uniquely identifies this logon session. The authentication package is responsible for allocating this <b>LUID</b>, and creating the logon session for this logon.


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
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.


### -param TokenInformationType [out]

Pointer that receives the address of an 
<a href="https://msdn.microsoft.com/c8bf5b8d-6cb1-469d-a451-6cceafda24cf">LSA_TOKEN_INFORMATION_TYPE</a> value that indicates the type of information returned for inclusion in the token to be created. The information is returned in the <i>TokenInformation</i> buffer.


### -param *TokenInformation [out]

Pointer that receives information to be included in the token. The format and content of the <i>TokenInformation</i> buffer are indicated by the <i>TokenInformationType</i> parameter. Your authentication package is responsible for allocating the memory used by <i>TokenInformation</i>; however, this memory will be freed by the LSA.


### -param *AccountName [out]

Pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that receives the name of the user account. <i>AccountName</i> must always be returned regardless of the success or failure of the call; its string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AccountName</i>; however, this memory will be freed by the LSA.


### -param *AuthenticatingAuthority [out]

Optional. Pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that receives the description of the authenticating authority for the logon. This parameter may be <b>NULL</b>. This string is included in the audit record for an authentication attempt. Your authentication package is responsible for allocating the memory used by <i>AuthenticatingAuthority</i>; however, this memory will be freed by the LSA. 




The MSV1_0 authentication package returns the domain name of the domain validating the account. The Kerberos authentication package returns the NetBIOS domain name.


## -returns



If the function succeeds, it should return STATUS_SUCCESS.

If the function fails, it should return an NTSTATUS error code, which can be one of the following values or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

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
The user account and password were legitimate, but user account restrictions prevent logon at this time. For additional information, see the <i>SubStatus</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_VALIDATION_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The authentication information provided is not recognized by the specified authentication package.

</td>
</tr>
</table>
 

Calling applications can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



Authentication packages must implement one of the following functions: <b>LsaApLogonUser</b>, 
<a href="https://msdn.microsoft.com/7778292a-7062-4f49-b4a9-6784e5e4ccd7">LsaApLogonUserEx</a>, or 
<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a>.




## -see-also




<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a>



<a href="https://msdn.microsoft.com/c8bf5b8d-6cb1-469d-a451-6cceafda24cf">LSA_TOKEN_INFORMATION_TYPE</a>



<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/7778292a-7062-4f49-b4a9-6784e5e4ccd7">LsaApLogonUserEx</a>



<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a>



<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>
 

 

