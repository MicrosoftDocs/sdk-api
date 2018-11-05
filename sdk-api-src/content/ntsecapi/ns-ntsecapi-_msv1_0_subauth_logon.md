---
UID: NS:ntsecapi._MSV1_0_SUBAUTH_LOGON
title: "_MSV1_0_SUBAUTH_LOGON"
author: windows-sdk-content
description: Used by subauthentication DLLs.
old-location: security\msv1_0_subauth_logon.htm
tech.root: secauthn
ms.assetid: e53cb14a-097c-4ee4-ab7a-baa4b6699cc7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PMSV1_0_SUBAUTH_LOGON, MSV1_0_ALLOW_SERVER_TRUST_ACCOUNT, MSV1_0_ALLOW_WORKSTATION_TRUST_ACCOUNT, MSV1_0_CLEARTEXT_PASSWORD_ALLOWED, MSV1_0_DONT_TRY_GUEST_ACCOUNT, MSV1_0_RETURN_PASSWORD_EXPIRY, MSV1_0_RETURN_PROFILE_PATH, MSV1_0_RETURN_USER_PARAMETERS, MSV1_0_SUBAUTH_LOGON, MSV1_0_SUBAUTH_LOGON structure [Security], MSV1_0_TRY_GUEST_ACCOUNT_ONLY, MSV1_0_TRY_SPECIFIED_DOMAIN_ONLY, MSV1_0_UPDATE_LOGON_STATISTICS, PMSV1_0_SUBAUTH_LOGON, PMSV1_0_SUBAUTH_LOGON structure pointer [Security], _MSV1_0_SUBAUTH_LOGON, _lsa_msv1_0_subauth_logon, ntsecapi/MSV1_0_SUBAUTH_LOGON, ntsecapi/PMSV1_0_SUBAUTH_LOGON, security.msv1_0_subauth_logon"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
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
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - MSV1_0_SUBAUTH_LOGON
product: Windows
targetos: Windows
req.typenames: MSV1_0_SUBAUTH_LOGON, *PMSV1_0_SUBAUTH_LOGON
req.redist: 
---

# _MSV1_0_SUBAUTH_LOGON structure


## -description


The <b>MSV1_0_SUBAUTH_LOGON</b> structure is used by <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication</a> DLLs.


## -struct-fields




### -field MessageType

A 
						<a href="https://msdn.microsoft.com/03bf43f0-44f4-40c6-8d5d-381f36ebdd0e">MSV1_0_LOGON_SUBMIT_TYPE</a> value that indicates the type of logon being requested. This value must be set to <b>MsV1_0SubAuthLogon</b>.


### -field LogonDomainName

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> that contains the name of the logon domain. The specified domain name must be a Windows domain or a mixed domain that is trusted by this computer. If the logon domain name is not known (for example, for clients that do not supply this information), this member should be passed in as a zero-length string. This is the authenticating authority.


### -field UserName

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> that contains the account name of the user. The name can be up to 255 bytes long. The name is treated as case insensitive.


### -field Workstation

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> that contains the computer name of the workstation where the user logon request was initiated.


### -field ChallengeToClient

Contains the challenge returned from a previous call to 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>, when <b>MsV1_0Lm20ChallengeRequest</b> was specified as the message type. For more information, see the description of <b>MsV1_0Lm20ChallengeRequest</b> in 
<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>. This enables the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> to determine whether the challenge response is correct.


### -field AuthenticationInfo1

Contains <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a>–specific information. For more information, see the subauthentication package documentation.


### -field AuthenticationInfo2

Contains subauthentication package specific information. For more information, see the subauthentication package documentation.


### -field ParameterControl

Specifies additional information about how the logon should be processed. This member can contain one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_CLEARTEXT_PASSWORD_ALLOWED"></a><a id="msv1_0_cleartext_password_allowed"></a><dl>
<dt><b>MSV1_0_CLEARTEXT_PASSWORD_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
LanMan2.0 or LanMan1.0 send a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a> password instead of a challenge response. To allow plaintext passwords to be used in the NetworkLogon message, an application must supply this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_UPDATE_LOGON_STATISTICS"></a><a id="msv1_0_update_logon_statistics"></a><dl>
<dt><b>MSV1_0_UPDATE_LOGON_STATISTICS</b></dt>
</dl>
</td>
<td width="60%">
Update the logon statistics for the account. If this flag is not set, the bad password count is set to zero upon successful logon.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_RETURN_USER_PARAMETERS"></a><a id="msv1_0_return_user_parameters"></a><dl>
<dt><b>MSV1_0_RETURN_USER_PARAMETERS</b></dt>
</dl>
</td>
<td width="60%">
Causes the user parameters to be returned in the <b>HomeDirectoryDrive</b> member of the 
<a href="https://msdn.microsoft.com/70592c29-0810-4d3b-bc5a-73165582a94b">MSV1_0_INTERACTIVE_PROFILE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_DONT_TRY_GUEST_ACCOUNT"></a><a id="msv1_0_dont_try_guest_account"></a><dl>
<dt><b>MSV1_0_DONT_TRY_GUEST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Prevents the user from logging on with a guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_ALLOW_SERVER_TRUST_ACCOUNT"></a><a id="msv1_0_allow_server_trust_account"></a><dl>
<dt><b>MSV1_0_ALLOW_SERVER_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, domain controller accounts can be used for authentication; otherwise, only user accounts can be used.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_RETURN_PASSWORD_EXPIRY"></a><a id="msv1_0_return_password_expiry"></a><dl>
<dt><b>MSV1_0_RETURN_PASSWORD_EXPIRY</b></dt>
</dl>
</td>
<td width="60%">
Causes the password expiration time to be returned in the <b>LogoffTime</b> member of the 
<a href="https://msdn.microsoft.com/4bf69171-1f92-40df-ab0f-cd6790ce34f1">MSV1_0_LM20_LOGON_PROFILE</a> structure returned in the output buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_ALLOW_WORKSTATION_TRUST_ACCOUNT"></a><a id="msv1_0_allow_workstation_trust_account"></a><dl>
<dt><b>MSV1_0_ALLOW_WORKSTATION_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
 Permits remote-boot clients to log on using a computer account.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_TRY_GUEST_ACCOUNT_ONLY"></a><a id="msv1_0_try_guest_account_only"></a><dl>
<dt><b>MSV1_0_TRY_GUEST_ACCOUNT_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Causes the user to log on using the guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_RETURN_PROFILE_PATH"></a><a id="msv1_0_return_profile_path"></a><dl>
<dt><b>MSV1_0_RETURN_PROFILE_PATH</b></dt>
</dl>
</td>
<td width="60%">
Returns the profile path associated with the logged on user.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_TRY_SPECIFIED_DOMAIN_ONLY"></a><a id="msv1_0_try_specified_domain_only"></a><dl>
<dt><b>MSV1_0_TRY_SPECIFIED_DOMAIN_ONLY</b></dt>
</dl>
</td>
<td width="60%">
 Only a domain controller associated with the specified domain will attempt to validate the logon request.

</td>
</tr>
</table>
 


### -field SubAuthPackageId

Contains the subauthentication package identifier. This value is set by the subauthentication package vendor.


## -see-also




<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/70592c29-0810-4d3b-bc5a-73165582a94b">MSV1_0_INTERACTIVE_PROFILE</a>



<a href="https://msdn.microsoft.com/4bf69171-1f92-40df-ab0f-cd6790ce34f1">MSV1_0_LM20_LOGON_PROFILE</a>



<a href="https://msdn.microsoft.com/03bf43f0-44f4-40c6-8d5d-381f36ebdd0e">MSV1_0_LOGON_SUBMIT_TYPE</a>



<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>
 

 

