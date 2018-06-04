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

# SHSetUnreadMailCountW function


## -description


Stores the current user's unread message count for a specified email account in the registry.


## -parameters




### -param pszMailAddress [in]

Type: <b>LPCTSTR</b>

A pointer to a string in Unicode that contains the current user's full email address.


### -param dwCount

Type: <b>DWORD</b>

The number of unread messages.


### -param pszShellExecuteCommand [in]

Type: <b>LPCTSTR</b>

A pointer to a string in Unicode that contains the full text of a command that can be passed to ShellExecute. This command should start the email application that owns the account referenced by <i>pszMailAddress</i>.


## -returns



Type: <b>HRESULT</b>

<b>HRESULT</b>, which includes the following possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid string argument in either the <i>pszMailAddress</i> or <i>pszShellExecuteCommand</i> parameters.

</td>
</tr>
</table>
 




## -remarks



When this function updates the registry, the new registry entry is automatically stamped with the current time and date.

If this function is called by different independent software vendors (ISVs) that specify the same email name, only the last call is saved. That is, calls to this function overwrite any previously saved value for the same email address, even if the calls are made by different ISVs.

It is recommended that the count of unread messages be set only for the main Inbox of the users account. Mail in sub-folders such as Drafts or Deleted Items should be ignored.

It is important that email clients do not set the number of unread messages to 0 when the application exits, because this causes the number of unread messages to be erroneously reported as 0.

Because this function uses HKEY_CURRENT_USER, it should not be called by a system process impersonating a user.



