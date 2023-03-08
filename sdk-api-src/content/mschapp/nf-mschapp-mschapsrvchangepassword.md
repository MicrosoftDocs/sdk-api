---
UID: NF:mschapp.MSChapSrvChangePassword
title: MSChapSrvChangePassword function (mschapp.h)
description: Changes the password of a user account.
helpviewer_keywords: ["MSChapSrvChangePassword","MSChapSrvChangePassword function [MS-CHAP]","_mschap_mschapsrvchangepassword","mschap.mschapsrvchangepassword","mschapp/MSChapSrvChangePassword"]
old-location: mschap\mschapsrvchangepassword.htm
tech.root: MsChap
ms.assetid: 6c154675-4c82-4305-8231-577f990eaeb1
ms.date: 12/05/2018
ms.keywords: MSChapSrvChangePassword, MSChapSrvChangePassword function [MS-CHAP], _mschap_mschapsrvchangepassword, mschap.mschapsrvchangepassword, mschapp/MSChapSrvChangePassword
req.header: mschapp.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MSChapSrvChangePassword
 - mschapp/MSChapSrvChangePassword
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - MSChapSrvChangePassword
---

# MSChapSrvChangePassword function


## -description

The 
<b>MSChapSrvChangePassword</b> function changes the password of a user account.

## -parameters

### -param ServerName [in]

A pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) name of the server on which to operate. If this parameter is <b>NULL</b>, the function operates on the local computer.

### -param UserName [in]

A pointer to a null-terminated Unicode string that specifies the name of the user whose password is being changed.

### -param LmOldPresent [in]

A <b>BOOLEAN</b> that specifies whether the password designated by <i>LmOldOwfPassword</i> is valid. <i>LmOldPresent</i> is <b>FALSE</b> if the <i>LmOldOwfPassword</i> password is greater than 128-bits in length, and therefore cannot be represented by a Lan Manager (LM) one-way function (OWF) password. Otherwise, it is <b>TRUE</b>.

### -param LmOldOwfPassword [in]

A pointer to a <a href="/windows/desktop/api/mschapp/ns-mschapp-lm_owf_password">LM_OWF_PASSWORD</a> structure that contains the OWF of the user's current LM  password. This parameter is ignored if <i>LmOldPresent</i> is <b>FALSE</b>.

### -param LmNewOwfPassword [in]

A pointer to a <a href="/windows/desktop/api/mschapp/ns-mschapp-lm_owf_password">LM_OWF_PASSWORD</a> structure that contains the OWF of the user's new LM password.

### -param NtOldOwfPassword [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/cc325731(v=vs.85)">NT_OWF_PASSWORD</a> structure that contains the OWF of the user's current NT password.

### -param NtNewOwfPassword [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/cc325731(v=vs.85)">NT_OWF_PASSWORD</a> structure that contains the OWF of the user's new NT password.

## -returns

If the function succeeds, the return value is <b>STATUS_SUCCESS (0x00000000)</b>.

If the function fails, the return value is one of the following error codes from ntstatus.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
<dt>0xC0000022</dt>
</dl>
</td>
<td width="60%">
The calling application does not have the appropriate privilege to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
<dt>0xC0000008</dt>
</dl>
</td>
<td width="60%">
The specified server or user name was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ILL_FORMED_PASSWORD</b></dt>
<dt>0xC000006B</dt>
</dl>
</td>
<td width="60%">
New password is poorly formed, for example, it contains characters that cannot be entered from the keyboard.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PASSWORD_RESTRICTION</b></dt>
<dt>0xC000006C</dt>
</dl>
</td>
<td width="60%">
A restriction prevents the password from being changed. Possible restrictions include time restrictions on how often a password is allowed to be changed or length restrictions on the provided password. This error is also returned if the new password matched a password in the recent history log for the account. Security administrators specify how many of the most recently used passwords are not available for re-use. These are kept in the password recent history log.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_WRONG_PASSWORD</b></dt>
<dt>0xC000006A</dt>
</dl>
</td>
<td width="60%">
The old password parameter does not match the user's current password.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_STATE</b></dt>
<dt>0xC00000DD</dt>
</dl>
</td>
<td width="60%">
The domain controller is not in an enabled state. The domain controller must be enabled for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_ROLE</b></dt>
<dt>0xC00000DE</dt>
</dl>
</td>
<td width="60%">
The domain controller is serving in the incorrect role to perform the requested operation. The operation can only be performed by the primary domain controller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER_MIX</b></dt>
<dt>0xC0000030</dt>
</dl>
</td>
<td width="60%">
The value of the <i>LmOldPresent</i> parameter is not correct for the contents of the old and new  parameter pairs.

</td>
</tr>
</table>

## -remarks

The value specified by <i>LmNewOwfPassword</i> must always contain a valid OWF. If the new password is greater than 128-bits long, and therefore cannot be represented by a LAN Manager (LM) password, then <i>LmNewOwfPassword</i> should be the LM OWF of a <b>NULL</b> password.

This function allows users to change their own passwords only if they have the access: <a href="/windows/win32/adschema/r-user-change-password">USER_CHANGE_PASSWORD</a>.

This function fails with <b>STATUS_PASSWORD_RESTRICTION</b> if the attempt to change the password conflicts with an administrative password restriction.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-functions">MS-CHAP Password Management Functions</a>



<a href="/previous-versions/windows/desktop/api/mschapp/nf-mschapp-mschapsrvchangepassword2">MSChapSrvChangePassword2</a>