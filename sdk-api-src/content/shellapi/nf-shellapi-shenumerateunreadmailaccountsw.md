---
UID: NF:shellapi.SHEnumerateUnreadMailAccountsW
title: SHEnumerateUnreadMailAccountsW function (shellapi.h)
description: Enumerates the user accounts that have unread email.helpviewer_keywords: ["SHEnumerateUnreadMailAccounts","SHEnumerateUnreadMailAccounts function [Windows Shell]","SHEnumerateUnreadMailAccountsA","SHEnumerateUnreadMailAccountsW","_shell_SHEnumerateUnreadMailAccounts","shell.SHEnumerateUnreadMailAccounts","shellapi/SHEnumerateUnreadMailAccounts","shellapi/SHEnumerateUnreadMailAccountsA","shellapi/SHEnumerateUnreadMailAccountsW"]
old-location: shell\SHEnumerateUnreadMailAccounts.htm
tech.root: shell
ms.assetid: 67ec8355-f902-4b71-972f-94e403701f96
ms.date: 12/05/2018
ms.keywords: SHEnumerateUnreadMailAccounts, SHEnumerateUnreadMailAccounts function [Windows Shell], SHEnumerateUnreadMailAccountsA, SHEnumerateUnreadMailAccountsW, _shell_SHEnumerateUnreadMailAccounts, shell.SHEnumerateUnreadMailAccounts, shellapi/SHEnumerateUnreadMailAccounts, shellapi/SHEnumerateUnreadMailAccountsA, shellapi/SHEnumerateUnreadMailAccountsW
f1_keywords:
- shellapi/SHEnumerateUnreadMailAccounts
dev_langs:
- c++
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
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHEnumerateUnreadMailAccountsW function


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



