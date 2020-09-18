---
UID: NS:ntsecapi._KERB_INTERACTIVE_PROFILE
title: KERB_INTERACTIVE_PROFILE (ntsecapi.h)
description: The KERB_INTERACTIVE_PROFILE structure contains information about an interactive logon profile. This structure is used by the LsaLogonUser function.
helpviewer_keywords: ["*PKERB_INTERACTIVE_PROFILE","KERB_INTERACTIVE_PROFILE","KERB_INTERACTIVE_PROFILE structure [Security]","LOGON_EXTRA_SIDS","LOGON_RESOURCE_GROUPS","PKERB_INTERACTIVE_PROFILE","PKERB_INTERACTIVE_PROFILE structure pointer [Security]","_lsa_kerb_interactive_profile","ntsecapi/KERB_INTERACTIVE_PROFILE","ntsecapi/PKERB_INTERACTIVE_PROFILE","security.kerb_interactive_profile"]
old-location: security\kerb_interactive_profile.htm
tech.root: security
ms.assetid: 8e9dd04b-8155-4f85-be00-ff9d8297deaa
ms.date: 12/05/2018
ms.keywords: '*PKERB_INTERACTIVE_PROFILE, KERB_INTERACTIVE_PROFILE, KERB_INTERACTIVE_PROFILE structure [Security], LOGON_EXTRA_SIDS, LOGON_RESOURCE_GROUPS, PKERB_INTERACTIVE_PROFILE, PKERB_INTERACTIVE_PROFILE structure pointer [Security], _lsa_kerb_interactive_profile, ntsecapi/KERB_INTERACTIVE_PROFILE, ntsecapi/PKERB_INTERACTIVE_PROFILE, security.kerb_interactive_profile'
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
targetos: Windows
req.typenames: KERB_INTERACTIVE_PROFILE, *PKERB_INTERACTIVE_PROFILE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_INTERACTIVE_PROFILE
 - ntsecapi/_KERB_INTERACTIVE_PROFILE
 - PKERB_INTERACTIVE_PROFILE
 - ntsecapi/PKERB_INTERACTIVE_PROFILE
 - KERB_INTERACTIVE_PROFILE
 - ntsecapi/KERB_INTERACTIVE_PROFILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_INTERACTIVE_PROFILE
---

# KERB_INTERACTIVE_PROFILE structure


## -description

The <b>KERB_INTERACTIVE_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is used by the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_profile_buffer_type">KERB_PROFILE_BUFFER_TYPE</a> value identifying the type of logon request being made. This member can be set to <b>KerbInteractiveProfile</b>.

### -field LogonCount

Number of times the user is currently logged on.

### -field BadPasswordCount

Number of times a bad password was applied to the account since the last successful logon.

### -field LogonTime

Time when the user last logged on. This is an absolute-format standard time value.

### -field LogoffTime

Time when user should log off. This is an absolute-format standard time value.

### -field KickOffTime

Time when system should force user logoff. This is an absolute-format standard time value.

### -field PasswordLastSet

Time and date the password was last set. This is an absolute-format standard time value.

### -field PasswordCanChange

Time and date when the user can change the password. This is an absolute-format standard time value. To prevent a password from ever changing, set this member to a date very far into the future.

### -field PasswordMustChange

Time and date when the user must change the password. If the user can never change the password, this member is undefined. This is an absolute-format standard time value.

### -field LogonScript

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the relative path to the account's logon script.

### -field HomeDirectory

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the user's home directory.

### -field FullName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the user's full name.

### -field ProfilePath

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the path to a user's roaming profile. This is used only if the user has a roaming profile.

### -field HomeDirectoryDrive

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the drive containing the user's home directory.

### -field LogonServer

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the server that processed the logon request.

### -field UserFlags

Specifies how this user established the session. This can be one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_EXTRA_SIDS"></a><a id="logon_extra_sids"></a><dl>
<dt><b>LOGON_EXTRA_SIDS</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using extra <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_RESOURCE_GROUPS"></a><a id="logon_resource_groups"></a><dl>
<dt><b>LOGON_RESOURCE_GROUPS</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using a domain local group.

</td>
</tr>
</table>