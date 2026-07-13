---
UID: NF:shlwapi.SHGetValueW
title: SHGetValueW function (shlwapi.h)
description: Retrieves a registry value. (SHGetValueW)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHGetValue", "SHGetValue function [Windows Shell]", "SHGetValueW", "_win32_SHGetValue", "shell.SHGetValue", "shlwapi/SHGetValue", "shlwapi/SHGetValueW"]
old-location: shell\SHGetValue.htm
tech.root: shell
ms.assetid: 8cca6bfe-d365-4d10-bc8d-f3bebefaad02
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHGetValue, SHGetValue function [Windows Shell], SHGetValueA, SHGetValueW, _win32_SHGetValue, shell.SHGetValue, shlwapi/SHGetValue, shlwapi/SHGetValueA, shlwapi/SHGetValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetValueW (Unicode) and SHGetValueA (ANSI)
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
 - SHGetValueW
 - shlwapi/SHGetValueW
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
 - SHGetValue
 - SHGetValueA
 - SHGetValueW
---

# SHGetValueW function


## -description

Retrieves a registry value.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

A handle to the currently open key, or any of the following predefined values.



#### HKEY_CLASSES_ROOT



#### HKEY_CURRENT_CONFIG



#### HKEY_CURRENT_USER



#### HKEY_LOCAL_MACHINE



#### HKEY_PERFORMANCE_DATA



#### HKEY_USERS

### -param pszSubKey [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the name of the subkey from which to retrieve the value.

### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

The address of the value.

### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

The type of value. For more information, see <a href="/windows/desktop/shell/hkey-type">Registry Data Types</a>.

### -param pvData [out, optional]

Type: <b>LPVOID</b>

The address of the destination data buffer.

### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

The size of the destination data buffer.


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

If your application must set/retrieve a series of values in the same key, it is better to open the key once and set/retrieve the values with the regular Microsoft Win32 registry functions rather than use this function repeatedly.




> [!NOTE]
> The shlwapi.h header defines SHGetValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
