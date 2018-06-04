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



