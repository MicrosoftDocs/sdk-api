---
UID: NC:ntsecapi.PSAM_PASSWORD_FILTER_ROUTINE
title: PSAM_PASSWORD_FILTER_ROUTINE
author: windows-sdk-content
description: Implemented by a password filter DLL. The value returned by this function determines whether the new password is accepted by the system.
old-location: security\passwordfilter.htm
old-project: SecMgmt
ms.assetid: cb4fe40e-81ea-4040-b3ee-642a093e5fca
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: PSAM_PASSWORD_FILTER_ROUTINE, PSAM_PASSWORD_FILTER_ROUTINE callback, PasswordFilter, PasswordFilter callback function [Security], _pswd_passwordfilter, ntsecapi/PasswordFilter, security.passwordfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: CI_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecapi.h
api_name:
-	PasswordFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSAM_PASSWORD_FILTER_ROUTINE callback function


## -description



			The <b>PasswordFilter</b> function is implemented by a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">password filter</a> DLL. The value returned by this function determines whether the new password is accepted by the system. All of the password filters installed on a system must return <b>TRUE</b> for the password change to take effect.


## -parameters




### -param AccountName [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that represents the name of the user whose password changed.


### -param FullName [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that represents the full name of the user whose password changed.


### -param Password [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that represents the new plaintext password. When you have finished using the password, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information on protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


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
Return <b>TRUE</b> if the new password is valid with respect to the password policy implemented in the password filter DLL. When <b>TRUE</b> is returned, the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) continues to evaluate the password by calling any other password filters installed on the system.

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

This function is called only for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">password filters</a> that are installed and registered on a system.

Any process exception that is not handled within this function may cause security-related failures system-wide. Structured exception handling should be used when appropriate.

<table>
<tr>
<th>For information about</th>
<th>See</th>
</tr>
<tr>
<td>Programming issues when implementing a password filter DLL</td>
<td>
<a href="https://msdn.microsoft.com/ec7c1e7e-844a-43d4-b756-02bc1062d7b8">Password Filter Programming Considerations</a>
</td>
</tr>
<tr>
<td>How to install and register your own password filter DLL</td>
<td>
<a href="https://msdn.microsoft.com/12a6fe6d-5b37-4fcf-bd04-0a22d84ba323">Installing and Registering a Password Filter DLL</a>
</td>
</tr>
<tr>
<td>The password filter DLL provided by Microsoft </td>
<td>
<a href="https://msdn.microsoft.com/a84f83b2-181b-4f65-82bd-bc7f0689aad3">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c503c849-65da-4514-b6d9-a95c9d75433e">InitializeChangeNotify</a>



<a href="https://msdn.microsoft.com/81d34dff-3842-407b-8fd8-3b0a5a5f38f1">PasswordChangeNotify</a>
 

 

