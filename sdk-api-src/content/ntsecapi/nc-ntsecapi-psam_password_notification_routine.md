---
UID: NC:ntsecapi.PSAM_PASSWORD_NOTIFICATION_ROUTINE
title: PSAM_PASSWORD_NOTIFICATION_ROUTINE (ntsecapi.h)
description: Is implemented by a password filter DLL. It notifies the DLL that a password was changed.
helpviewer_keywords: ["PSAM_PASSWORD_NOTIFICATION_ROUTINE","PSAM_PASSWORD_NOTIFICATION_ROUTINE callback","PasswordChangeNotify","PasswordChangeNotify callback function [Security]","_pswd_passwordchangenotify","ntsecapi/PasswordChangeNotify","security.passwordchangenotify"]
old-location: security\passwordchangenotify.htm
tech.root: security
ms.assetid: 81d34dff-3842-407b-8fd8-3b0a5a5f38f1
ms.date: 12/05/2018
ms.keywords: PSAM_PASSWORD_NOTIFICATION_ROUTINE, PSAM_PASSWORD_NOTIFICATION_ROUTINE callback, PasswordChangeNotify, PasswordChangeNotify callback function [Security], _pswd_passwordchangenotify, ntsecapi/PasswordChangeNotify, security.passwordchangenotify
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSAM_PASSWORD_NOTIFICATION_ROUTINE
 - ntsecapi/PSAM_PASSWORD_NOTIFICATION_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecapi.h
api_name:
 - PasswordChangeNotify
---

# PSAM_PASSWORD_NOTIFICATION_ROUTINE callback function


## -description

The <b>PasswordChangeNotify</b> function is implemented by a <a href="/windows/desktop/SecGloss/p-gly">password filter</a> DLL. It notifies the DLL that a password was changed.

## -parameters

### -param UserName [in]

The account name of the user whose password changed.

If the values of this parameter and the <i>NewPassword</i> parameter are <b>NULL</b>, this function should return <b>STATUS_SUCCESS</b>.

### -param RelativeId [in]

The <a href="/windows/desktop/SecGloss/r-gly">relative identifier</a> (RID) of the user specified in <i>UserName</i>.

### -param NewPassword [in]

A new plaintext password for the user specified in <i>UserName</i>. When you have finished using the password, clear the information by calling the  <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

If the values of this parameter and the <i>UserName</i> parameter are <b>NULL</b>, this function should return <b>STATUS_SUCCESS</b>.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
Indicates the password of the user was changed, or that the values of both the <i>UserName</i> and <i>NewPassword</i> parameters are <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>PasswordChangeNotify</b> function is called after the <a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_password_filter_routine">PasswordFilter</a> function has been called successfully and the new password has been stored.

This function must use the __stdcall calling convention and must be exported by the DLL.

When the <b>PasswordChangeNotify</b> routine is running, processing is blocked until the routine is finished. When appropriate, move any lengthy processing to a separate thread prior to returning from this routine.

This function is called only for <a href="/windows/desktop/SecGloss/p-gly">password filters</a> that are installed and registered on the system.

Any process exception that is not handled within this function may cause security-related failures system-wide. Structured exception handling should be used when appropriate.

<table>
<tr>
<th>For information about</th>
<th>See</th>
</tr>
<tr>
<td>Programming issues when implementing a password filter DLL</td>
<td>
<a href="/windows/desktop/SecMgmt/password-filter-programming-considerations">Password Filter Programming Considerations</a>
</td>
</tr>
<tr>
<td>How to install and register your own password filter DLL</td>
<td>
<a href="/windows/desktop/SecMgmt/installing-and-registering-a-password-filter-dll">Installing and Registering a Password Filter DLL</a>
</td>
</tr>
<tr>
<td>The password filter DLL provided by Microsoft</td>
<td>
<a href="/windows/desktop/SecMgmt/strong-password-enforcement-and-passfilt-dll">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_init_notification_routine">InitializeChangeNotify</a>



<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_password_filter_routine">PasswordFilter</a>