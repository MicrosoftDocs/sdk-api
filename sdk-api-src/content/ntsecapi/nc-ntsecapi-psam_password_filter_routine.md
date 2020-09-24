---
UID: NC:ntsecapi.PSAM_PASSWORD_FILTER_ROUTINE
title: PSAM_PASSWORD_FILTER_ROUTINE (ntsecapi.h)
description: Implemented by a password filter DLL. The value returned by this function determines whether the new password is accepted by the system.
helpviewer_keywords: ["PSAM_PASSWORD_FILTER_ROUTINE","PSAM_PASSWORD_FILTER_ROUTINE callback","PasswordFilter","PasswordFilter callback function [Security]","_pswd_passwordfilter","ntsecapi/PasswordFilter","security.passwordfilter"]
old-location: security\passwordfilter.htm
tech.root: security
ms.assetid: cb4fe40e-81ea-4040-b3ee-642a093e5fca
ms.date: 12/05/2018
ms.keywords: PSAM_PASSWORD_FILTER_ROUTINE, PSAM_PASSWORD_FILTER_ROUTINE callback, PasswordFilter, PasswordFilter callback function [Security], _pswd_passwordfilter, ntsecapi/PasswordFilter, security.passwordfilter
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
 - PSAM_PASSWORD_FILTER_ROUTINE
 - ntsecapi/PSAM_PASSWORD_FILTER_ROUTINE
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
 - PasswordFilter
---

# PSAM_PASSWORD_FILTER_ROUTINE callback function


## -description

The <b>PasswordFilter</b> function is implemented by a <a href="/windows/desktop/SecGloss/p-gly">password filter</a> DLL. The value returned by this function determines whether the new password is accepted by the system. All of the password filters installed on a system must return <b>TRUE</b> for the password change to take effect.

## -parameters

### -param AccountName [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that represents the name of the user whose password changed.

### -param FullName [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that represents the full name of the user whose password changed.

### -param Password [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that represents the new plaintext password. When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information on protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param SetOperation [in]

<b>TRUE</b> if the password was set rather than changed.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>TRUE</b> if the new password is valid with respect to the password policy implemented in the password filter DLL. When <b>TRUE</b> is returned, the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) continues to evaluate the password by calling any other password filters installed on the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>FALSE</b> if the new password is not valid with respect to the password policy implemented in the password filter DLL. When <b>FALSE</b> is returned, the LSA returns the ERROR_ILL_FORMED_PASSWORD (1324) status code to the source of the password change request.

</td>
</tr>
</table>

## -remarks

Password change requests may be made when users specify a new password, accounts are created and when administrators override a password.

This function must use the __stdcall calling convention and must be exported by the DLL.

When the <b>PasswordFilter</b> routine is running, processing is blocked until the routine is finished. When appropriate, move any lengthy processing to a separate thread prior to returning from this routine.

This function is called only for <a href="/windows/desktop/SecGloss/p-gly">password filters</a> that are installed and registered on a system.

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
<td>The password filter DLL provided by Microsoft </td>
<td>
<a href="/windows/desktop/SecMgmt/strong-password-enforcement-and-passfilt-dll">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_init_notification_routine">InitializeChangeNotify</a>



<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_password_notification_routine">PasswordChangeNotify</a>