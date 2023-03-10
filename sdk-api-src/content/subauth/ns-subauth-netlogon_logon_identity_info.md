---
UID: NS:subauth._NETLOGON_LOGON_IDENTITY_INFO
title: NETLOGON_LOGON_IDENTITY_INFO (subauth.h)
description: Used to pass information about a user for logon subauthentication.
helpviewer_keywords: ["*PNETLOGON_LOGON_IDENTITY_INFO","CLEARTEXT_PASSWORD_ALLOWED","NETLOGON_LOGON_IDENTITY_INFO","NETLOGON_LOGON_IDENTITY_INFO structure [Security]","PNETLOGON_LOGON_IDENTITY_INFO","PNETLOGON_LOGON_IDENTITY_INFO structure pointer [Security]","_lsa_netlogon_logon_identity_info","security.netlogon_logon_identity_info","subauth/NETLOGON_LOGON_IDENTITY_INFO","subauth/PNETLOGON_LOGON_IDENTITY_INFO"]
old-location: security\netlogon_logon_identity_info.htm
tech.root: security
ms.assetid: b9cdf09f-897c-407e-80ba-e18c9ba667ec
ms.date: 12/05/2018
ms.keywords: '*PNETLOGON_LOGON_IDENTITY_INFO, CLEARTEXT_PASSWORD_ALLOWED, NETLOGON_LOGON_IDENTITY_INFO, NETLOGON_LOGON_IDENTITY_INFO structure [Security], PNETLOGON_LOGON_IDENTITY_INFO, PNETLOGON_LOGON_IDENTITY_INFO structure pointer [Security], _lsa_netlogon_logon_identity_info, security.netlogon_logon_identity_info, subauth/NETLOGON_LOGON_IDENTITY_INFO, subauth/PNETLOGON_LOGON_IDENTITY_INFO'
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
req.typenames: NETLOGON_LOGON_IDENTITY_INFO, *PNETLOGON_LOGON_IDENTITY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETLOGON_LOGON_IDENTITY_INFO
 - subauth/_NETLOGON_LOGON_IDENTITY_INFO
 - PNETLOGON_LOGON_IDENTITY_INFO
 - subauth/PNETLOGON_LOGON_IDENTITY_INFO
 - NETLOGON_LOGON_IDENTITY_INFO
 - subauth/NETLOGON_LOGON_IDENTITY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Subauth.h
api_name:
 - NETLOGON_LOGON_IDENTITY_INFO
---

# NETLOGON_LOGON_IDENTITY_INFO structure


## -description

The <b>NETLOGON_LOGON_IDENTITY_INFO</b> structure is used to pass information about a user for logon <a href="/windows/desktop/SecGloss/s-gly">subauthentication</a>.

It is used by 
<a href="/windows/desktop/api/subauth/nf-subauth-msv1_0subauthenticationroutine">Msv1_0SubAuthenticationRoutine</a> and 
<a href="/windows/desktop/api/subauth/nf-subauth-msv1_0subauthenticationfilter">Msv1_0SubAuthenticationFilter</a>.

## -struct-fields

### -field LogonDomainName

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the logon domain. The specified domain name must be a domain that is trusted by this machine. If the logon domain is unknown, such as a down-level client that does not supply this information, this member should be <b>NULL</b>.

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
Specifies that <b>CaseSensitiveChallengeResponse</b> and <b>CaseInsensitiveChallengeResponse</b> are allowed to be the user's <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> password.

</td>
</tr>
</table>

### -field LogonId

Uniquely identifies the <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

### -field UserName

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> identifying the account name of the user attempting to log on.

### -field Workstation

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> identifying the workstation from which the user is attempting to log on. <b>NULL</b> indicates that the workstation identity is unknown.