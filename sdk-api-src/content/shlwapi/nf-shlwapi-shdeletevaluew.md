---
UID: NF:shlwapi.SHDeleteValueW
title: SHDeleteValueW function (shlwapi.h)
description: Deletes a named value from the specified registry key. (Unicode)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHDeleteValue", "SHDeleteValue function [Windows Shell]", "SHDeleteValueW", "_win32_SHDeleteValue", "shell.SHDeleteValue", "shlwapi/SHDeleteValue", "shlwapi/SHDeleteValueW"]
old-location: shell\SHDeleteValue.htm
tech.root: shell
ms.assetid: 54f3459b-486c-4907-84b1-39b1f8abb12d
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHDeleteValue, SHDeleteValue function [Windows Shell], SHDeleteValueA, SHDeleteValueW, _win32_SHDeleteValue, shell.SHDeleteValue, shlwapi/SHDeleteValue, shlwapi/SHDeleteValueA, shlwapi/SHDeleteValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHDeleteValueW (Unicode) and SHDeleteValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHDeleteValueW
 - shlwapi/SHDeleteValueW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-Registry-l1-1-0.dll
 - API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
 - SHDeleteValue
 - SHDeleteValueA
 - SHDeleteValueW
---

# SHDeleteValueW function


## -description

Deletes a named value from the specified registry key.

## -parameters

### -param hkey

Type: <b>HKEY</b>

A handle to the currently open key, or any of the following predefined values.



#### HKEY_CLASSES_ROOT



#### HKEY_CURRENT_CONFIG



#### HKEY_CURRENT_USER



#### HKEY_LOCAL_MACHINE



#### HKEY_PERFORMANCE_DATA



#### HKEY_USERS

### -param pszSubKey

Type: <b>LPCTSTR</b>

The address of a null-terminated string specifying the name of the subkey for which to change the value.

### -param pszValue

Type: <b>LPCTSTR</b>

The address of the value to be deleted.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHDeleteValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
