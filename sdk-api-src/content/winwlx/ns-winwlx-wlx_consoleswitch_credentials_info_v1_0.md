---
UID: NS:winwlx._WLX_CONSOLESWITCH_CREDENTIALS_INFO
title: WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 (winwlx.h)
description: Contains the client credentials returned by a call to WlxGetConsoleSwitchCredentials.
helpviewer_keywords: ["*PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0","LOGON_EXTRA_SIDS","PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0","PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 structure pointer [Security]","WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0","WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 structure [Security]","_gina_wlx_consoleswitch_credentials_info_v1_0","security.wlx_consoleswitch_credentials_info_v1_0","winwlx/PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0","winwlx/WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0"]
old-location: security\wlx_consoleswitch_credentials_info_v1_0.htm
tech.root: security
ms.assetid: f72f3dd3-42a3-4f2b-be36-13c496c396fd
ms.date: 12/05/2018
ms.keywords: '*PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0, LOGON_EXTRA_SIDS, PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0, PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 structure pointer [Security], WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0, WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 structure [Security], _gina_wlx_consoleswitch_credentials_info_v1_0, security.wlx_consoleswitch_credentials_info_v1_0, winwlx/PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0, winwlx/WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0'
req.header: winwlx.h
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
req.typenames: WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0, *PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_CONSOLESWITCH_CREDENTIALS_INFO
 - winwlx/_WLX_CONSOLESWITCH_CREDENTIALS_INFO
 - PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
 - winwlx/PWLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
 - WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
 - winwlx/WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0
---

# WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0 structure


## -description

The <b>WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</b> structure contains the client credentials returned by a call to 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxgetconsoleswitchcredentials">WlxGetConsoleSwitchCredentials</a>.

This allows credentials to be transparently transferred to a target session.

## -struct-fields

### -field dwType

Identifies the type of credentials structure being allocated. Credential types are defined with the prefix WLX_CONSOLESWITCHCREDENTIAL_TYPE allowing Winlogon to typecast the structure so the remainder of the structure may be referenced.

### -field UserToken

Handle of the users token.

### -field LogonId

Unique logon identifier.

### -field Quotas

QUOTA_LIMITS structure containing information on the amount of system resources available to a user.

### -field UserName

User's name as a string.

### -field Domain

User's domain as a string.

### -field LogonTime

Exact logon time.

### -field SmartCardLogon

<b>TRUE</b> if the logon was done by SmartCard.

### -field ProfileLength

Length of the user's profile in bytes.

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type">MSV1_0_PROFILE_BUFFER_TYPE</a> value identifying the type of profile data being returned. This member must be set to <b>MsV1_0InteractiveProfile</b>.

### -field LogonCount

Number of times the user is currently logged on. 




<div class="alert"><b>Note</b>  This value is not guaranteed to be accurate because the domain controller is not notified of all logons and logoffs.</div>
<div> </div>

### -field BadPasswordCount

Number of times a password that is not valid was applied to the account since the last successful logon.

### -field ProfileLogonTime

Time when the user last logged on. This is an absolute-format Windows standard time value.

### -field LogoffTime

Time when user should log off. This is an absolute-format Windows standard time value.

### -field KickOffTime

Time when system should force the user to log off. This is an absolute-format Windows standard time value. Note that Windows users are not forced to log off interactively; however, their network connections may be closed.

### -field PasswordLastSet

Time and date the password was last changed. This is an absolute format Windows standard time value.

### -field PasswordCanChange

Time and date when the user should be reminded to change passwords. This is an absolute-format Windows standard time value. This member is used by the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to display the prompt asking whether the user wants to change the current password.

### -field PasswordMustChange

Time and date when the user must change the password. If the user can never change the password, this member is undefined. This is an absolute-format, Windows, standard time value.

### -field LogonScript

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the relative path to the account's logon script.

### -field HomeDirectory

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the home directory for the user.

### -field FullName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the full name of the user.

### -field ProfilePath

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the path to the user's roaming profile if the user has a roaming profile. For example: \\SomeServer\SomeShare\MyUserName

### -field HomeDirectoryDrive

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the drive letter (for example, C:\ or D:\) of the home directory.

### -field LogonServer

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the server that processed the logon request.

### -field UserFlags

Specifies how this user established the session. This can be the following flag.

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
The user logged on using extra <a href="/windows/desktop/SecGloss/s-gly">SIDs</a>.

</td>
</tr>
</table>

### -field PrivateDataLen

Length in bytes of any GINA-specific data. Set to zero if there is no GINA specific data.

### -field PrivateData

Buffer containing any GINA-specific data.