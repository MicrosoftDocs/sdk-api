---
UID: NF:shellapi.SHEnumerateUnreadMailAccountsA
title: SHEnumerateUnreadMailAccountsA function
author: windows-sdk-content
description: Enumerates the user accounts that have unread email.
old-location: shell\SHEnumerateUnreadMailAccounts.htm
old-project: shell
ms.assetid: 67ec8355-f902-4b71-972f-94e403701f96
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHEnumerateUnreadMailAccounts, SHEnumerateUnreadMailAccounts function [Windows Shell], SHEnumerateUnreadMailAccountsA, SHEnumerateUnreadMailAccountsW, _shell_SHEnumerateUnreadMailAccounts, shell.SHEnumerateUnreadMailAccounts, shellapi/SHEnumerateUnreadMailAccounts, shellapi/SHEnumerateUnreadMailAccountsA, shellapi/SHEnumerateUnreadMailAccountsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHEnumerateUnreadMailAccountsW (Unicode) and SHEnumerateUnreadMailAccountsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHEnumerateUnreadMailAccounts
 - SHEnumerateUnreadMailAccountsA
 - SHEnumerateUnreadMailAccountsW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# SHEnumerateUnreadMailAccountsA function


## -description


Enumerates the user accounts that have unread email.


## -parameters




### -param hKeyUser [in, optional]

Type: <b>HKEY</b>

A valid HKEY for a given user.


### -param dwIndex

Type: <b>DWORD</b>

The index of the user account.


### -param pszMailAddress [out]

Type: <b>LPTSTR</b>

A pointer to a Unicode string that specifies the email address of an account belonging to the specified user.


### -param cchMailAddress

Type: <b>int</b>

The number of characters in the email address.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>hKeyUser</i> parameter is the HKEY for the root of the user's information, for example <b>HKEY_CURRENT_USER</b>, or any key enumerated under <b>HKEY_USERS</b>.



