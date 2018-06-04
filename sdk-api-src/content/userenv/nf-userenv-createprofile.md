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



