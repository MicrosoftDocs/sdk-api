---
UID: NS:ntsecapi._MSV1_0_LM20_LOGON_PROFILE
title: "_MSV1_0_LM20_LOGON_PROFILE"
author: windows-sdk-content
description: Contains information about a network logon session.
old-location: security\msv1_0_lm20_logon_profile.htm
tech.root: secauthn
ms.assetid: 4bf69171-1f92-40df-ab0f-cd6790ce34f1
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PMSV1_0_LM20_LOGON_PROFILE, LOGON_CACHED_ACCOUNT, LOGON_EXTRA_SIDS, LOGON_GUEST, LOGON_NOENCRYPTION, LOGON_PROFILE_PATH_RETURNED, LOGON_RESOURCE_GROUPS, LOGON_SERVER_TRUST_ACCOUNT, LOGON_SUBAUTH_SESSION_KEY, LOGON_USED_LM_PASSWORD, MSV1_0_LM20_LOGON_PROFILE, MSV1_0_LM20_LOGON_PROFILE structure [Security], PMSV1_0_LM20_LOGON_PROFILE, PMSV1_0_LM20_LOGON_PROFILE structure pointer [Security], _MSV1_0_LM20_LOGON_PROFILE, _lsa_msv1_0_lm20_logon_profile, ntsecapi/MSV1_0_LM20_LOGON_PROFILE, ntsecapi/PMSV1_0_LM20_LOGON_PROFILE, security.msv1_0_lm20_logon_profile"
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
 - MSV1_0_LM20_LOGON_PROFILE
product: Windows
targetos: Windows
req.typenames: MSV1_0_LM20_LOGON_PROFILE, *PMSV1_0_LM20_LOGON_PROFILE
req.redist: 
---

# _MSV1_0_LM20_LOGON_PROFILE structure


## -description


The <b>MSV1_0_LM20_LOGON_PROFILE</b> structure contains information about a network <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.

It is used by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/c8fe967a-e172-4200-ab15-daebf441c689">MSV1_0_PROFILE_BUFFER_TYPE</a> value identifying the type of logon requested. The type of logon determines the format and content of the profile data returned. This member must be set to <b>MsV1_0LM20LogonProfile</b>.


### -field KickOffTime

Time when the system should force user logoff. This is an absolute-format Windows standard time value.


### -field LogoffTime

Time when the user should log off. This is an absolute-format Windows standard time value.


### -field UserFlags

Specifies the way the user established the session. <b>UserFlags</b> can contain one or more of the following values. 





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
The user logged onto a guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_NOENCRYPTION"></a><a id="logon_noencryption"></a><dl>
<dt><b>LOGON_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The user logged on without using password encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_CACHED_ACCOUNT"></a><a id="logon_cached_account"></a><dl>
<dt><b>LOGON_CACHED_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using cached <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_USED_LM_PASSWORD"></a><a id="logon_used_lm_password"></a><dl>
<dt><b>LOGON_USED_LM_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using an LM password instead of a Windows password. An LM password is the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashed</a> version of the MBCS upper-cased password.

The Windows password is the hashed version of the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> password.

The caller may need to know which type of password was used to determine the corresponding <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> (<b>LanmanSessionKey</b> or UserSessionKey). 

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_EXTRA_SIDS"></a><a id="logon_extra_sids"></a><dl>
<dt><b>LOGON_EXTRA_SIDS</b></dt>
</dl>
</td>
<td width="60%">
SIDs from a domain other than the user's logon domain were sent back from the user's domain controller. This information is used internally by the LSA.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_SUBAUTH_SESSION_KEY"></a><a id="logon_subauth_session_key"></a><dl>
<dt><b>LOGON_SUBAUTH_SESSION_KEY</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication</a> session key.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_SERVER_TRUST_ACCOUNT"></a><a id="logon_server_trust_account"></a><dl>
<dt><b>LOGON_SERVER_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using a trusted server account.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_PROFILE_PATH_RETURNED"></a><a id="logon_profile_path_returned"></a><dl>
<dt><b>LOGON_PROFILE_PATH_RETURNED</b></dt>
</dl>
</td>
<td width="60%">
The profile path in the profile in the <b>UserParameters</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_RESOURCE_GROUPS"></a><a id="logon_resource_groups"></a><dl>
<dt><b>LOGON_RESOURCE_GROUPS</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using resource groups.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The high-order byte of <b>UserFlags</b> is reserved for return flags from <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication packages</a>. The flags returned by a subauthentication package are package specific. For more information, see the documentation for the subauthentication package.</div>
<div> </div>

### -field UserSessionKey

Contains a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> specific to the session and user. This session key can be used to encrypt and decrypt information sent between the client and server. This string is MSV1_0_USER_SESSION_KEY_LENGTH characters long. The array is not null-terminated and can contain embedded null characters.


### -field LogonDomainName


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing the name of the logon domain.


### -field LanmanSessionKey

Contains the Lanman session key. This string is MSV1_0_LANMAN_SESSION_KEY_LENGTH characters long. It is not null-terminated and can contain embedded null characters.


### -field LogonServer


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing the name of the server that processed the logon request.


### -field UserParameters


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing user parameters. These parameters are primarily used by RAS to store RAS dial-in permissions for the user. In general, developers should not modify this member.


## -see-also




<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>



<a href="https://msdn.microsoft.com/c8fe967a-e172-4200-ab15-daebf441c689">MSV1_0_PROFILE_BUFFER_TYPE</a>
 

 

