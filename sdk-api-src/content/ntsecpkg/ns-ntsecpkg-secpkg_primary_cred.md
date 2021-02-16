---
UID: NS:ntsecpkg._SECPKG_PRIMARY_CRED
title: SECPKG_PRIMARY_CRED (ntsecpkg.h)
description: The SECPKG_PRIMARY_CRED structure contains the primary credentials. This structure is used by the LsaApLogonUserEx2 and SpAcceptCredentials functions.
helpviewer_keywords: ["*PSECPKG_PRIMARY_CRED","PRIMARY_CRED_CACHED_LOGON","PRIMARY_CRED_CLEAR_PASSWORD","PRIMARY_CRED_OWF_PASSWORD","PRIMARY_CRED_UPDATE","PSECPKG_PRIMARY_CRED","PSECPKG_PRIMARY_CRED structure pointer [Security]","SECPKG_PRIMARY_CRED","SECPKG_PRIMARY_CRED structure [Security]","_ssp_secpkg_primary_cred","ntsecpkg/PSECPKG_PRIMARY_CRED","ntsecpkg/SECPKG_PRIMARY_CRED","security.secpkg_primary_cred"]
old-location: security\secpkg_primary_cred.htm
tech.root: security
ms.assetid: e51fd400-6c3c-4861-ab5c-6c1800b12d31
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_PRIMARY_CRED, PRIMARY_CRED_CACHED_LOGON, PRIMARY_CRED_CLEAR_PASSWORD, PRIMARY_CRED_OWF_PASSWORD, PRIMARY_CRED_UPDATE, PSECPKG_PRIMARY_CRED, PSECPKG_PRIMARY_CRED structure pointer [Security], SECPKG_PRIMARY_CRED, SECPKG_PRIMARY_CRED structure [Security], _ssp_secpkg_primary_cred, ntsecpkg/PSECPKG_PRIMARY_CRED, ntsecpkg/SECPKG_PRIMARY_CRED, security.secpkg_primary_cred'
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
req.typenames: SECPKG_PRIMARY_CRED, *PSECPKG_PRIMARY_CRED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_PRIMARY_CRED
 - ntsecpkg/_SECPKG_PRIMARY_CRED
 - PSECPKG_PRIMARY_CRED
 - ntsecpkg/PSECPKG_PRIMARY_CRED
 - SECPKG_PRIMARY_CRED
 - ntsecpkg/SECPKG_PRIMARY_CRED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_PRIMARY_CRED
---

# SECPKG_PRIMARY_CRED structure


## -description

The <b>SECPKG_PRIMARY_CRED</b> structure contains the <a href="/windows/desktop/SecGloss/p-gly">primary credentials</a>. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn">SpAcceptCredentials</a> functions.

## -struct-fields

### -field LogonId

The <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a>.

### -field DownlevelName

A 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the Security Accounts Manager account name.

### -field DomainName

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the NetBIOS domain name where the account is located.

### -field Password

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the logon password. When you have finished using the password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information on protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -field OldPassword

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the old password. When you have finished using the old password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>.

### -field UserSid

Pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a>.

### -field Flags

The set of <a href="/windows/desktop/SecGloss/p-gly">primary credentials</a> flags. The following table lists the valid values for the <b>Flags</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_CLEAR_PASSWORD"></a><a id="primary_cred_clear_password"></a><dl>
<dt><b>PRIMARY_CRED_CLEAR_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The passwords are in plaintext.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_OWF_PASSWORD"></a><a id="primary_cred_owf_password"></a><dl>
<dt><b>PRIMARY_CRED_OWF_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The passwords are encrypted using a one-way function.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_UPDATE"></a><a id="primary_cred_update"></a><dl>
<dt><b>PRIMARY_CRED_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
This is a change of existing credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_CACHED_LOGON"></a><a id="primary_cred_cached_logon"></a><dl>
<dt><b>PRIMARY_CRED_CACHED_LOGON</b></dt>
</dl>
</td>
<td width="60%">
The credentials were obtained from a cached logon. For more information, see Remarks.

</td>
</tr>
</table>

### -field DnsDomainName

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the DNS domain name where the user account is located, if known.

### -field Upn

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the user principal name (UPN), if known.

### -field LogonServer

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name of the server that processed the logon.

### -field Spare1

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure. Reserved.

### -field Spare2

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure. Reserved.

### -field Spare3

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure. Reserved.

### -field Spare4

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure. Reserved.

## -remarks

For cached logons, the RPC identifier of the package that performs the logon is identified by shifting the <b>Flags</b> member to the right by using the PRIMARY_CRED_LOGON_PACKAGE_SHIFT constant defined below.


```cpp
#define PRIMARY_CRED_LOGON_PACKAGE_SHIFT 24

```