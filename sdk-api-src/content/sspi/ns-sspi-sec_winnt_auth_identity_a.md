---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_A
title: SEC_WINNT_AUTH_IDENTITY_A (sspi.h)
description: Allows you to pass a particular user name and password to the run-time library for the purpose of authentication. (ANSI)
helpviewer_keywords: ["*PSEC_WINNT_AUTH_IDENTITY_A","PSEC_WINNT_AUTH_IDENTITY","PSEC_WINNT_AUTH_IDENTITY structure pointer [Security]","SEC_WINNT_AUTH_IDENTITY","SEC_WINNT_AUTH_IDENTITY structure [Security]","SEC_WINNT_AUTH_IDENTITY_A","SEC_WINNT_AUTH_IDENTITY_ANSI","SEC_WINNT_AUTH_IDENTITY_UNICODE","SEC_WINNT_AUTH_IDENTITY_W","_SEC_WINNT_AUTH_IDENTITY_A","_SEC_WINNT_AUTH_IDENTITY_W","_ssp_sec_winnt_auth_identity","security.sec_winnt_auth_identity","sspi/PSEC_WINNT_AUTH_IDENTITY","sspi/SEC_WINNT_AUTH_IDENTITY"]
old-location: security\sec_winnt_auth_identity.htm
tech.root: security
ms.assetid: a9c9471b-2134-4173-af86-18b277627d2a
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_IDENTITY_A, PSEC_WINNT_AUTH_IDENTITY, PSEC_WINNT_AUTH_IDENTITY structure pointer [Security], SEC_WINNT_AUTH_IDENTITY, SEC_WINNT_AUTH_IDENTITY structure [Security], SEC_WINNT_AUTH_IDENTITY_A, SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_UNICODE, SEC_WINNT_AUTH_IDENTITY_W, _SEC_WINNT_AUTH_IDENTITY_A, _SEC_WINNT_AUTH_IDENTITY_W, _ssp_sec_winnt_auth_identity, security.sec_winnt_auth_identity, sspi/PSEC_WINNT_AUTH_IDENTITY, sspi/SEC_WINNT_AUTH_IDENTITY'
req.header: sspi.h
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
req.typenames: SEC_WINNT_AUTH_IDENTITY_A, *PSEC_WINNT_AUTH_IDENTITY_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_A
 - sspi/_SEC_WINNT_AUTH_IDENTITY_A
 - PSEC_WINNT_AUTH_IDENTITY_A
 - sspi/PSEC_WINNT_AUTH_IDENTITY_A
 - SEC_WINNT_AUTH_IDENTITY_A
 - sspi/SEC_WINNT_AUTH_IDENTITY_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_IDENTITY
 - SEC_WINNT_AUTH_IDENTITY_A
 - SEC_WINNT_AUTH_IDENTITY_W
---

# SEC_WINNT_AUTH_IDENTITY_A structure


## -description

Allows you to pass a particular user name and password to the run-time library for the purpose of authentication.

## -struct-fields

### -field User

A string that contains the user name.

### -field UserLength

The length, in characters, of the user string, not including the terminating null character.

### -field Domain

A string that contains the domain name or the workgroup name.

### -field DomainLength

The length, in characters, of the domain string, not including the terminating null character.

### -field Password

A string that contains the password of the user in the domain or workgroup. When you have finished using the password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -field PasswordLength

The length, in characters, of the password string, not including the terminating null character.

### -field Flags

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a><a id="sec_winnt_auth_identity_ansi"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ANSI</b></dt>
</dl>
</td>
<td width="60%">
The strings in this structure are in ANSI format. 

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a><a id="sec_winnt_auth_identity_unicode"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_UNICODE</b></dt>
</dl>
</td>
<td width="60%">
The strings in this structure are in <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> format.

</td>
</tr>
</table>

## -remarks

When this structure is used with RPC, the structure must remain valid for the lifetime of the binding handle.

The strings may be ANSI or Unicode, depending on the value you assign to the <b>Flags</b> member.
