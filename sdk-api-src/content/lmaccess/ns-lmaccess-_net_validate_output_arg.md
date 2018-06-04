---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _NET_VALIDATE_OUTPUT_ARG structure


## -description


The <b>NET_VALIDATE_OUTPUT_ARG</b> structure contains information about persistent password-related data that has changed since the user's last logon as well as the result of the function's password validation check.


## -struct-fields




### -field ChangedPersistedFields

A  structure that contains changes to persistent information about the account being logged on. For more information, see the following Remarks section.


### -field ValidationStatus

The result of the password validation check performed by the <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> function. The status depends on the value specified in the <i>ValidationType</i> parameter to that function.

<b>Authentication.</b> When you call <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> and specify the <i>ValidationType</i> parameter as NetValidateAuthentication, this member can be one of the following values.

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
 

<b>Password change.</b> When you call <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> and specify the <i>ValidationType</i> parameter as NetValidatePasswordChange, this member can be one of the following values.

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



The <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> function outputs the <b>NET_VALIDATE_OUTPUT_ARG</b> structure. 

Note that it is the application's responsibility to save all the data in the <b>ChangedPersistedFields</b> member of the <b>NET_VALIDATE_OUTPUT_ARG</b> structure as well as any User object information. The next time the application calls <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> on the same instance of the User object, the application must provide the required fields from the persistent information.




## -see-also




<a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

