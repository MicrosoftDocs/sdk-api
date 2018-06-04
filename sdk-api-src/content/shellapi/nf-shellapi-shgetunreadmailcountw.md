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

# SHGetUnreadMailCountW function


## -description


Retrieves a specified user's unread message count for any or all email accounts.


## -parameters




### -param hKeyUser [in, optional]

Type: <b>HKEY</b>

A valid HKEY for a given user. This parameter should be <b>NULL</b> if the function is called in a user's environment, in which case <b>HKEY_CURRENT_USER</b> is used. This parameter should be <b>NULL</b> if the function is called from the SYSTEM context, in which case <b>HKEY_USERS</b>\<i>{SID}</i> is used.


### -param pszMailAddress [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a string in Unicode that specifies the email address of an account belonging to the specified user. When this parameter is <b>NULL</b>, <i>pdwCount</i> returns the total count of unread messages for all accounts owned by the designated user.


### -param pdwCount [out, optional]

Type: <b>DWORD*</b>

Pointer to a DWORD value which receives the unread message count.


### -param pFileTime [out, optional]

Type: <b>FILETIME*</b>

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.  The use of this parameter is determined by whether <i>pszMailAddress</i> is <b>NULL</b>. If <i>pszMailAddress</i> is <b>NULL</b>, then this parameter is treated as an [in] parameter, which specifies a filter, so that only unread mail newer than the specified time appears. If <i>pszMailAddress</i> is not <b>NULL</b>, then this parameter is treated as an [out] parameter, which points to a <b>FILETIME</b> structure into which the function places the <b>timestamp</b> of the last <a href="https://msdn.microsoft.com/4a0e1ade-8df1-41b5-b6ea-dad427b50f5a">SHSetUnreadMailCount</a> call for the specified user and email account.


### -param pszShellExecuteCommand [out, optional]

Type: <b>LPCTSTR</b>

A pointer to a string that returns the ShellExecute command statement passed into the last <a href="https://msdn.microsoft.com/4a0e1ade-8df1-41b5-b6ea-dad427b50f5a">SHSetUnreadMailCount</a> call for the specified user and email account. This command string starts the email application that owns the account referenced by <i>pszMailAddress</i>. If the ShellExecute command is not required, this parameter can be <b>NULL</b>. If <i>pszMailAddress</i> is <b>NULL</b>, this parameter is ignored and must be <b>NULL</b>.


### -param cchShellExecuteCommand

Type: <b>int</b>

The maximum size, in characters, of the ShellExecute command buffer pointed to by <i>pszShellExecuteCommand</i>. This parameter must be zero for total counts when <i>pszMailAddress</i> is <b>NULL</b>. It can also be <b>NULL</b> whenever the ShellExecute command string is not required.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



