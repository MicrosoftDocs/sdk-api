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

# CryptUpdateProtectedState function


## -description


The <b>CryptUpdateProtectedState</b> function migrates the current user's master keys after the user's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) has changed. This function can be used to preserve encrypted data after a user has been moved from one domain to another.


## -parameters




### -param pOldSid [in]

The address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that contains the user's previous SID. This SID is used to locate the old master keys. If this parameter is <b>NULL</b>, the master keys for the current user SID are migrated.

Either this parameter or the <i>pwszOldPassword</i> parameter may be <b>NULL</b>, but not both.


### -param pwszOldPassword [in]

A pointer to a null-terminated Unicode string that contains the user's password before the SID was changed. This password is used to decrypt the old master keys. If this parameter is <b>NULL</b>, the password of the current user will be used.

Either this parameter or the <i>pOldSid</i> parameter may be <b>NULL</b>, but not both.


### -param dwFlags [in]

Not used. Must be zero.


### -param pdwSuccessCount [out]

The address of a <b>DWORD</b> variable that receives the number of master keys that were successfully migrated.


### -param pdwFailureCount [out]

The address of a <b>DWORD</b> variable that receives the number of master keys that could not be decrypted.

It is not necessarily an error if one or more master keys cannot be decrypted. Some users may possess master keys that are stagnant and could not have been decrypted for a long time. One way that this can happen is when the password of a local user has been administratively reset.


## -returns




						If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ENCRYPTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The old password could not be encrypted.

</td>
</tr>
</table>
 




## -remarks



This function decrypts all of the user's master keys in the old master key directory, using the previous password, and stores them in the user's current master key directory, encrypted with the user's current password.

 This function must be called from the user account that the keys are being migrated to.

If this function is able to successfully migrate an old master key, it will automatically delete the old master key. 
Master keys that cannot be decrypted are not deleted.



