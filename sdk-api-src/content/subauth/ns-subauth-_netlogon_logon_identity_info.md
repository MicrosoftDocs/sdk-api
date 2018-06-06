---
UID: NS:subauth._NETLOGON_LOGON_IDENTITY_INFO
title: "_NETLOGON_LOGON_IDENTITY_INFO"
author: windows-sdk-content
description: Used to pass information about a user for logon subauthentication.
old-location: security\netlogon_logon_identity_info.htm
old-project: SecAuthN
ms.assetid: b9cdf09f-897c-407e-80ba-e18c9ba667ec
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PNETLOGON_LOGON_IDENTITY_INFO, CLEARTEXT_PASSWORD_ALLOWED, NETLOGON_LOGON_IDENTITY_INFO, NETLOGON_LOGON_IDENTITY_INFO structure [Security], PNETLOGON_LOGON_IDENTITY_INFO, PNETLOGON_LOGON_IDENTITY_INFO structure pointer [Security], _NETLOGON_LOGON_IDENTITY_INFO, _lsa_netlogon_logon_identity_info, security.netlogon_logon_identity_info, subauth/NETLOGON_LOGON_IDENTITY_INFO, subauth/PNETLOGON_LOGON_IDENTITY_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: NETLOGON_LOGON_IDENTITY_INFO, *PNETLOGON_LOGON_IDENTITY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Subauth.h
api_name:
 - NETLOGON_LOGON_IDENTITY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _NETLOGON_LOGON_IDENTITY_INFO structure


## -description


The <b>NETLOGON_LOGON_IDENTITY_INFO</b> structure is used to pass information about a user for logon <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication</a>.

It is used by 
<a href="https://msdn.microsoft.com/18d0da59-026a-4951-8529-f7dbaab20d08">Msv1_0SubAuthenticationRoutine</a> and 
<a href="https://msdn.microsoft.com/d7162830-8cab-4ec1-afcb-7892f5e435d3">Msv1_0SubAuthenticationFilter</a>.


## -struct-fields




### -field LogonDomainName

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the logon domain. The specified domain name must be a domain that is trusted by this machine. If the logon domain is unknown, such as a down-level client that does not supply this information, this member should be <b>NULL</b>. 


### -field ParameterControl

Specifies attributes of the other function parameters. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLEARTEXT_PASSWORD_ALLOWED"></a><a id="cleartext_password_allowed"></a><dl>
<dt><b>CLEARTEXT_PASSWORD_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
Specifies that <b>CaseSensitiveChallengeResponse</b> and <b>CaseInsensitiveChallengeResponse</b> are allowed to be the user's <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a> password.

</td>
</tr>
</table>
 


### -field LogonId

Uniquely identifies the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.
					


### -field UserName

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> identifying the account name of the user attempting to log on.


### -field Workstation

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> identifying the workstation from which the user is attempting to log on. <b>NULL</b> indicates that the workstation identity is unknown.

