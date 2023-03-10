---
UID: NF:mschapp.MSChapSrvChangePassword2
title: MSChapSrvChangePassword2 function (mschapp.h)
description: The MSChapSrvChangePassword2 function changes the password of a user account while supporting mutual encryption.
helpviewer_keywords: ["MSChapSrvChangePassword2","MSChapSrvChangePassword2 function [MS-CHAP]","_mschap_mschapsrvchangepassword2","mschap.mschapsrvchangepassword2","mschapp/MSChapSrvChangePassword2"]
old-location: mschap\mschapsrvchangepassword2.htm
tech.root: MsChap
ms.assetid: 91ea4b98-79e4-4764-a580-a622d1491943
ms.date: 12/05/2018
ms.keywords: MSChapSrvChangePassword2, MSChapSrvChangePassword2 function [MS-CHAP], _mschap_mschapsrvchangepassword2, mschap.mschapsrvchangepassword2, mschapp/MSChapSrvChangePassword2
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
 - MSChapSrvChangePassword2
 - mschapp/MSChapSrvChangePassword2
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
 - MSChapSrvChangePassword2
---

# MSChapSrvChangePassword2 function


## -description

The 
<b>MSChapSrvChangePassword2</b> function changes the password of a user account while supporting mutual encryption.

## -parameters

### -param ServerName [in]

A pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) name of the server on which to operate. If this parameter is <b>NULL</b>, the function operates on the local computer.

### -param UserName [in]

A pointer to a null-terminated Unicode string that specifies the name of the user whose password is being changed.

### -param NewPasswordEncryptedWithOldNt [in]

A pointer to a <a href="/windows/desktop/api/mschapp/ns-mschapp-sampr_encrypted_user_password">SAMPR_ENCRYPTED_USER_PASSWORD</a> structure that contains the new clear text password encrypted using the current NT one-way function (OWF) password hash as the encryption key.

<div class="alert"><b>Note</b>  Use  the <b>NewPasswordEncryptedWithOldNtPasswordHash()</b> function as defined in <a href="https://www.ietf.org/rfc/rfc2433.txt">RFC 2433</a>, section A.11 to calculate the cipher for <i>NewPasswordEncryptedWithOldNt</i>.</div>
<div> </div>

### -param OldNtOwfPasswordEncryptedWithNewNt [in]

A pointer to an <a href="/previous-versions/windows/desktop/legacy/cc325729(v=vs.85)">ENCRYPTED_NT_OWF_PASSWORD</a> structure that contains the old NT OWF password hash encrypted using the new NT OWF password hash as the encryption key.

### -param LmPresent [in]

A <b>BOOLEAN</b> that specifies if the current Lan Manager (LM) or NT OWF password hashes are used as the encryption keys to generate the <i>NewPasswordEncryptedWithOldNt</i> and <i>OldNtOwfPasswordEncryptedWithNewNt</i> ciphers. If <b>TRUE</b>, the  LM OWF password hashes are used rather than the NT OWF password hashes.

### -param NewPasswordEncryptedWithOldLm [in]

A pointer to a <a href="/windows/desktop/api/mschapp/ns-mschapp-sampr_encrypted_user_password">SAMPR_ENCRYPTED_USER_PASSWORD</a> structure that contains the new clear text password encrypted using the current LM OWF password hash.

<div class="alert"><b>Note</b>  Use  the <b>NewPasswordEncryptedWithOldLmPasswordHash()</b> function as defined in <a href="https://www.ietf.org/rfc/rfc2433.txt">RFC 2433</a>, section A.15 to calculate the cipher for <i>NewPasswordEncryptedWithOldLm</i>.</div>
<div> </div>

### -param OldLmOwfPasswordEncryptedWithNewLmOrNt [in]

A pointer to a <a href="/windows/desktop/api/mschapp/ns-mschapp-encrypted_lm_owf_password">ENCRYPTED_LM_OWF_PASSWORD</a> structure that contains the current LM OWF password hash encrypted using the new LM OWF password hash.

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
</table>

## -remarks

This function allows users to change their own passwords only if they have the access: <a href="/windows/win32/adschema/r-user-change-password">USER_CHANGE_PASSWORD</a>.

This function fails with <b>STATUS_PASSWORD_RESTRICTION</b> if the attempt to change the password conflicts with an administrative password restriction.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-functions">MS-CHAP Password Management Functions</a>



<a href="/previous-versions/windows/desktop/api/mschapp/nf-mschapp-mschapsrvchangepassword">MSChapSrvChangePassword</a>