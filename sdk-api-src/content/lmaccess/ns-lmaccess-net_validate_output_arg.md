---
UID: NS:lmaccess._NET_VALIDATE_OUTPUT_ARG
title: NET_VALIDATE_OUTPUT_ARG (lmaccess.h)
description: The NET_VALIDATE_OUTPUT_ARG structure contains information about persistent password-related data that has changed since the user's last logon as well as the result of the function's password validation check.
helpviewer_keywords: ["*PNET_VALIDATE_OUTPUT_ARG","NET_VALIDATE_OUTPUT_ARG","NET_VALIDATE_OUTPUT_ARG structure [Network Management]","PNET_VALIDATE_OUTPUT_ARG","PNET_VALIDATE_OUTPUT_ARG structure pointer [Network Management]","lmaccess/NET_VALIDATE_OUTPUT_ARG","lmaccess/PNET_VALIDATE_OUTPUT_ARG","netmgmt.net_validate_output_arg"]
old-location: netmgmt\net_validate_output_arg.htm
tech.root: NetMgmt
ms.assetid: 833c89c3-34ba-485b-a310-1d709aa618cd
ms.date: 12/05/2018
ms.keywords: '*PNET_VALIDATE_OUTPUT_ARG, NET_VALIDATE_OUTPUT_ARG, NET_VALIDATE_OUTPUT_ARG structure [Network Management], PNET_VALIDATE_OUTPUT_ARG, PNET_VALIDATE_OUTPUT_ARG structure pointer [Network Management], lmaccess/NET_VALIDATE_OUTPUT_ARG, lmaccess/PNET_VALIDATE_OUTPUT_ARG, netmgmt.net_validate_output_arg'
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
req.typenames: NET_VALIDATE_OUTPUT_ARG, *PNET_VALIDATE_OUTPUT_ARG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_VALIDATE_OUTPUT_ARG
 - lmaccess/_NET_VALIDATE_OUTPUT_ARG
 - PNET_VALIDATE_OUTPUT_ARG
 - lmaccess/PNET_VALIDATE_OUTPUT_ARG
 - NET_VALIDATE_OUTPUT_ARG
 - lmaccess/NET_VALIDATE_OUTPUT_ARG
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
 - NET_VALIDATE_OUTPUT_ARG
---

# NET_VALIDATE_OUTPUT_ARG structure


## -description

The <b>NET_VALIDATE_OUTPUT_ARG</b> structure contains information about persistent password-related data that has changed since the user's last logon as well as the result of the function's password validation check.

## -struct-fields

### -field ChangedPersistedFields

A  structure that contains changes to persistent information about the account being logged on. For more information, see the following Remarks section.

### -field ValidationStatus

The result of the password validation check performed by the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> function. The status depends on the value specified in the <i>ValidationType</i> parameter to that function.

<b>Authentication.</b> When you call <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> and specify the <i>ValidationType</i> parameter as NetValidateAuthentication, this member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NERR_AccountLockedOut</td>
<td>Validation failed. The account is locked out. </td>
</tr>
<tr>
<td>NERR_PasswordMustChange</td>
<td>Validation failed. The password must change at the next logon. </td>
</tr>
<tr>
<td>NERR_PasswordExpired</td>
<td>Validation failed. The password has expired. </td>
</tr>
<tr>
<td>NERR_BadPassword</td>
<td>Validation failed. The password is invalid. </td>
</tr>
<tr>
<td>NERR_Success</td>
<td>The password passes the validation check.</td>
</tr>
</table>
 

<b>Password change.</b> When you call <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> and specify the <i>ValidationType</i> parameter as NetValidatePasswordChange, this member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NERR_AccountLockedOut</td>
<td>Validation failed. The account is locked out. </td>
</tr>
<tr>
<td>NERR_PasswordTooRecent</td>
<td>Validation failed. The password for the user is too recent to change. </td>
</tr>
<tr>
<td>NERR_BadPassword</td>
<td>Validation failed. The password is invalid. </td>
</tr>
<tr>
<td>NERR_PasswordHistConflict</td>
<td>Validation failed. The password cannot be used at this time. </td>
</tr>
<tr>
<td>NERR_PasswordTooShort</td>
<td>Validation failed. The password does not meet policy requirements because it is  too short. </td>
</tr>
<tr>
<td>NERR_PasswordTooLong</td>
<td>Validation failed. The password does not meet policy requirements because it is too long. </td>
</tr>
<tr>
<td>NERR_PasswordNotComplexEnough</td>
<td>Validation failed. The password does not meet policy requirements because it is  not complex enough. </td>
</tr>
<tr>
<td>NERR_PasswordFilterError</td>
<td>Validation failed. The password does not meet  the requirements of the password filter DLL. </td>
</tr>
<tr>
<td>NERR_Success</td>
<td>The password passes the validation check.</td>
</tr>
</table>
 

<b>Password reset.</b> When you call <b>NetValidatePasswordPolicy</b> and specify the <i>ValidationType</i> parameter as NetValidatePasswordReset, this member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NERR_PasswordTooShort</td>
<td>Validation failed. The password does not meet policy requirements because it is  too short.</td>
</tr>
<tr>
<td>NERR_PasswordTooLong</td>
<td>Validation failed. The password does not meet policy requirements because it is too long.</td>
</tr>
<tr>
<td>NERR_PasswordNotComplexEnough</td>
<td>Validation failed. The password does not meet policy requirements because it is  not complex enough.  </td>
</tr>
<tr>
<td>NERR_PasswordFilterError</td>
<td>Validation failed. The password does not meet  the requirements of the password filter DLL. </td>
</tr>
<tr>
<td>NERR_Success</td>
<td>The password passes the validation check.</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> function outputs the <b>NET_VALIDATE_OUTPUT_ARG</b> structure. 

Note that it is the application's responsibility to save all the data in the <b>ChangedPersistedFields</b> member of the <b>NET_VALIDATE_OUTPUT_ARG</b> structure as well as any User object information. The next time the application calls <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> on the same instance of the User object, the application must provide the required fields from the persistent information.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>