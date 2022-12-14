---
UID: NF:shellapi.SHSetUnreadMailCountA
tech.root: shell 
title: SHSetUnreadMailCountA
ms.date: 04/14/2021
targetos: Windows
description: Stores the current user's unread message count for a specified email account in the registry. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Shell32.dll (version 5.60 or later) 
req.header: shellapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Shell32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only] 
req.target-min-winversvr: Windows Server 2003 [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHSetUnreadMailCountA
 - SHSetUnreadMailCount
f1_keywords:
 - SHSetUnreadMailCountA
 - shellapi/SHSetUnreadMailCountA
 - SHSetUnreadMailCount
 - shellapi/SHSetUnreadMailCount
dev_langs:
 - c++
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
