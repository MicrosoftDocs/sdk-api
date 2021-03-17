---
UID: NF:userenv.CreateProfile
title: CreateProfile function (userenv.h)
description: Creates a new user profile.
helpviewer_keywords: ["CreateProfile","CreateProfile function [Windows Shell]","_shell_CreateProfile","shell.CreateProfile","userenv/CreateProfile"]
old-location: shell\CreateProfile.htm
tech.root: shell
ms.assetid: cab9e20b-d94c-42e5-ada9-27194f398bb3
ms.date: 12/05/2018
ms.keywords: CreateProfile, CreateProfile function [Windows Shell], _shell_CreateProfile, shell.CreateProfile, userenv/CreateProfile
req.header: userenv.h
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateProfile
 - userenv/CreateProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - CreateProfile
---

# CreateProfile function


## -description

Creates a new user profile.

## -parameters

### -param pszUserSid [in]

Type: <b>LPCWSTR</b>

Pointer to the SID of the user as a string.

### -param pszUserName [in]

Type: <b>LPCWSTR</b>

The user name of the new user. This name is used as the base name for the profile directory.

### -param pszProfilePath [out]

Type: <b>LPWSTR</b>

When this function returns, contains a pointer to the full path of the profile.

### -param cchProfilePath [in]

Type: <b>DWORD</b>

Size of the buffer pointed to by <i>pszProfilePath</i>, in characters.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a sufficient permission level to create the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
A profile already exists for the specified user.

</td>
</tr>
</table>

## -remarks

The caller must have administrator privileges to call this function.

