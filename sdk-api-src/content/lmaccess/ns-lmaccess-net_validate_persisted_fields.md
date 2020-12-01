---
UID: NS:lmaccess._NET_VALIDATE_PERSISTED_FIELDS
title: NET_VALIDATE_PERSISTED_FIELDS (lmaccess.h)
description: The NET_VALIDATE_PERSISTED_FIELDS structure contains information about a user's password properties.
helpviewer_keywords: ["*PNET_VALIDATE_PERSISTED_FIELDS","NET_VALIDATE_BAD_PASSWORD_COUNT","NET_VALIDATE_BAD_PASSWORD_TIME","NET_VALIDATE_LOCKOUT_TIME","NET_VALIDATE_PASSWORD_HISTORY","NET_VALIDATE_PASSWORD_HISTORY_LENGTH","NET_VALIDATE_PASSWORD_LAST_SET","NET_VALIDATE_PERSISTED_FIELDS","NET_VALIDATE_PERSISTED_FIELDS structure [Network Management]","PNET_VALIDATE_PERSISTED_FIELDS","PNET_VALIDATE_PERSISTED_FIELDS structure pointer [Network Management]","lmaccess/NET_VALIDATE_PERSISTED_FIELDS","lmaccess/PNET_VALIDATE_PERSISTED_FIELDS","netmgmt.net_validate_persisted_fields"]
old-location: netmgmt\net_validate_persisted_fields.htm
tech.root: NetMgmt
ms.assetid: 1e6ea28a-a007-4cd1-b5d6-686bcf019fa1
ms.date: 12/05/2018
ms.keywords: '*PNET_VALIDATE_PERSISTED_FIELDS, NET_VALIDATE_BAD_PASSWORD_COUNT, NET_VALIDATE_BAD_PASSWORD_TIME, NET_VALIDATE_LOCKOUT_TIME, NET_VALIDATE_PASSWORD_HISTORY, NET_VALIDATE_PASSWORD_HISTORY_LENGTH, NET_VALIDATE_PASSWORD_LAST_SET, NET_VALIDATE_PERSISTED_FIELDS, NET_VALIDATE_PERSISTED_FIELDS structure [Network Management], PNET_VALIDATE_PERSISTED_FIELDS, PNET_VALIDATE_PERSISTED_FIELDS structure pointer [Network Management], lmaccess/NET_VALIDATE_PERSISTED_FIELDS, lmaccess/PNET_VALIDATE_PERSISTED_FIELDS, netmgmt.net_validate_persisted_fields'
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: NET_VALIDATE_PERSISTED_FIELDS, *PNET_VALIDATE_PERSISTED_FIELDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_VALIDATE_PERSISTED_FIELDS
 - lmaccess/_NET_VALIDATE_PERSISTED_FIELDS
 - PNET_VALIDATE_PERSISTED_FIELDS
 - lmaccess/PNET_VALIDATE_PERSISTED_FIELDS
 - NET_VALIDATE_PERSISTED_FIELDS
 - lmaccess/NET_VALIDATE_PERSISTED_FIELDS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - NET_VALIDATE_PERSISTED_FIELDS
---

# NET_VALIDATE_PERSISTED_FIELDS structure


## -description

The <b>NET_VALIDATE_PERSISTED_FIELDS</b> structure contains information about a user's password properties. Input to and output from the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> function contain persistent password-related data. When the function outputs this structure, it identifies the persistent data that has changed in this call.

## -struct-fields

### -field PresentFields

Type: <b>ULONG</b>

A set of bit flags identifying the persistent password-related data that has changed. This member is valid only when this structure is output from the <b>NetValidatePasswordPolicy</b> function. This member is ignored when this structure is input to the function. For more information, see the following Remarks section.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_PASSWORD_LAST_SET"></a><a id="net_validate_password_last_set"></a><dl>
<dt><b>NET_VALIDATE_PASSWORD_LAST_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>PasswordLastSet</b> member contains a new value.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_BAD_PASSWORD_TIME"></a><a id="net_validate_bad_password_time"></a><dl>
<dt><b>NET_VALIDATE_BAD_PASSWORD_TIME</b></dt>
</dl>
</td>
<td width="60%">
The <b>BadPasswordTime</b> member contains a new value.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_LOCKOUT_TIME"></a><a id="net_validate_lockout_time"></a><dl>
<dt><b>NET_VALIDATE_LOCKOUT_TIME</b></dt>
</dl>
</td>
<td width="60%">
The <b>LockoutTime</b> member contains a new value.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_BAD_PASSWORD_COUNT"></a><a id="net_validate_bad_password_count"></a><dl>
<dt><b>NET_VALIDATE_BAD_PASSWORD_COUNT</b></dt>
</dl>
</td>
<td width="60%">
The <b>BadPasswordCount</b> member contains a new value.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_PASSWORD_HISTORY_LENGTH"></a><a id="net_validate_password_history_length"></a><dl>
<dt><b>NET_VALIDATE_PASSWORD_HISTORY_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The <b>PasswordHistoryLength</b> member contains a new value.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_VALIDATE_PASSWORD_HISTORY"></a><a id="net_validate_password_history"></a><dl>
<dt><b>NET_VALIDATE_PASSWORD_HISTORY</b></dt>
</dl>
</td>
<td width="60%">
The <b>PasswordHistory</b> member contains a new value.

</td>
</tr>
</table>

### -field PasswordLastSet

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

The date and time (in GMT) when the password for the account was set or last changed.

### -field BadPasswordTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

The date and time (in GMT) when the user tried to log on to the account using an incorrect password.

### -field LockoutTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

The date and time (in GMT) when the account was last locked out. If the account has not been locked out, this member is zero. A lockout occurs when the number of bad password logins exceeds the number allowed.

### -field BadPasswordCount

Type: <b>ULONG</b>

The number of times the user tried to log on to the account using an incorrect password.

### -field PasswordHistoryLength

Type: <b>ULONG</b>

The number of previous passwords saved in the history list for the account. The user cannot reuse a password in the history list.

### -field PasswordHistory

Type: <b>PNET_VALIDATE_PASSWORD_HASH</b>

A pointer to a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_password_hash">NET_VALIDATE_PASSWORD_HASH</a> structure that contains the password hashes in the history list.

## -remarks

Note that it is the application's responsibility to save all changed persistent data as well as any user object information. The next time the application calls <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> on the same instance of the user object, the application must provide the required fields from the persistent information.

The <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_authentication_input_arg">NET_VALIDATE_AUTHENTICATION_INPUT_ARG</a>, <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a>, <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_password_reset_input_arg">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a>, and <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_output_arg">NET_VALIDATE_OUTPUT_ARG</a> structures contain a <b>NET_VALIDATE_PERSISTED_FIELDS</b> structure.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>