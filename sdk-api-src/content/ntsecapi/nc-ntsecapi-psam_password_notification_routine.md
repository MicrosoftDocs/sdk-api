---
UID: NC:ntsecapi.PSAM_PASSWORD_NOTIFICATION_ROUTINE
title: PSAM_PASSWORD_NOTIFICATION_ROUTINE
author: windows-sdk-content
description: Is implemented by a password filter DLL. It notifies the DLL that a password was changed.
old-location: security\passwordchangenotify.htm
old-project: secmgmt
ms.assetid: 81d34dff-3842-407b-8fd8-3b0a5a5f38f1
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: PSAM_PASSWORD_NOTIFICATION_ROUTINE, PSAM_PASSWORD_NOTIFICATION_ROUTINE callback, PasswordChangeNotify, PasswordChangeNotify callback function [Security], _pswd_passwordchangenotify, ntsecapi/PasswordChangeNotify, security.passwordchangenotify
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
tech.root: 
req.typenames: CI_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecapi.h
api_name:
 - PasswordChangeNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PSAM_PASSWORD_NOTIFICATION_ROUTINE callback function


## -description



			The <b>PasswordChangeNotify</b> function is implemented by a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">password filter</a> DLL. It notifies the DLL that a password was changed.


## -parameters




### -param UserName [in]

The account name of the user whose password changed.

If the values of this parameter and the <i>NewPassword</i> parameter are <b>NULL</b>, this function should return <b>STATUS_SUCCESS</b>.


### -param RelativeId [in]

The <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative identifier</a> (RID) of the user specified in <i>UserName</i>.


### -param NewPassword [in]

A new plaintext password for the user specified in <i>UserName</i>. When you have finished using the password, clear the information by calling the  <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.

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



The <b>PasswordChangeNotify</b> function is called after the <a href="https://msdn.microsoft.com/cb4fe40e-81ea-4040-b3ee-642a093e5fca">PasswordFilter</a> function has been called successfully and the new password has been stored.

This function must use the __stdcall calling convention and must be exported by the DLL.

When the <b>PasswordChangeNotify</b> routine is running, processing is blocked until the routine is finished. When appropriate, move any lengthy processing to a separate thread prior to returning from this routine.

This function is called only for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">password filters</a> that are installed and registered on the system.

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
<td>The password filter DLL provided by Microsoft</td>
<td>
<a href="https://msdn.microsoft.com/a84f83b2-181b-4f65-82bd-bc7f0689aad3">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c503c849-65da-4514-b6d9-a95c9d75433e">InitializeChangeNotify</a>



<a href="https://msdn.microsoft.com/cb4fe40e-81ea-4040-b3ee-642a093e5fca">PasswordFilter</a>
 

 

