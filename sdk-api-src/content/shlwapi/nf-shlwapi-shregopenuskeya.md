---
UID: NF:shlwapi.SHRegOpenUSKeyA
title: SHRegOpenUSKeyA function
author: windows-sdk-content
description: Opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegOpenUSKey.htm
tech.root: shell
ms.assetid: 756430a9-a495-412e-95c3-a93222bc467a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHRegOpenUSKey, SHRegOpenUSKey function [Windows Shell], SHRegOpenUSKeyA, SHRegOpenUSKeyW, _win32_SHRegOpenUSKey, shell.SHRegOpenUSKey, shlwapi/SHRegOpenUSKey, shlwapi/SHRegOpenUSKeyA, shlwapi/SHRegOpenUSKeyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegOpenUSKeyW (Unicode) and SHRegOpenUSKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-Registryuserspecific-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - SHRegOpenUSKey
 - SHRegOpenUSKeyA
 - SHRegOpenUSKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHRegOpenUSKeyA function


## -description


Opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the subkey.


### -param samDesired [in]

Type: <b><a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a></b>

The desired security access. For more information on security access, see <a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a>.


### -param hRelativeUSKey [in, optional]

Type: <b>HUSKEY</b>

The key to be used as a base for relative paths. If <i>pszPath</i> is a relative path, the key it specifies will be relative to <i>hRelativeUSKey</i>. If <i>pszPath</i> is an absolute path, set <i>hRelativeUSKey</i> to <b>NULL</b>.


### -param phNewUSKey [out]

Type: <b>PHUSKEY</b>

A pointer to the handle of the opened key.


### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

The variable that specifies which key to look under. When set to <b>TRUE</b>, <b>SHRegOpenUSKey</b> ignores <b>HKEY_CURRENT_USER</b> and returns a value from <b>HKEY_LOCAL_MACHINE</b>.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



