---
UID: NF:dpapi.CryptUpdateProtectedState
title: CryptUpdateProtectedState function (dpapi.h)
description: Migrates the current user's master keys after the user's security identifier (SID) has changed.
helpviewer_keywords: ["CryptUpdateProtectedState","CryptUpdateProtectedState function [Security]","dpapi/CryptUpdateProtectedState","security.cryptupdateprotectedstate","wincrypt/CryptUpdateProtectedState"]
old-location: security\cryptupdateprotectedstate.htm
tech.root: security
ms.assetid: f32e8fcd-6b5b-4a43-b3f9-77e17c84deca
ms.date: 12/05/2018
ms.keywords: CryptUpdateProtectedState, CryptUpdateProtectedState function [Security], dpapi/CryptUpdateProtectedState, security.cryptupdateprotectedstate, wincrypt/CryptUpdateProtectedState
req.header: dpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptUpdateProtectedState
 - dpapi/CryptUpdateProtectedState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptUpdateProtectedState
---

# CryptUpdateProtectedState function


## -description

The <b>CryptUpdateProtectedState</b> function migrates the current user's master keys after the user's <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) has changed. This function can be used to preserve encrypted data after a user has been moved from one domain to another.

## -parameters

### -param pOldSid [in]

The address of a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the user's previous SID. This SID is used to locate the old master keys. If this parameter is <b>NULL</b>, the master keys for the current user SID are migrated.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes include the following.

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