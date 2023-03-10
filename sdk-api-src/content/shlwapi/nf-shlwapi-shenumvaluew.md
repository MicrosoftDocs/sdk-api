---
UID: NF:shlwapi.SHEnumValueW
title: SHEnumValueW function (shlwapi.h)
description: Enumerates the values of the specified open registry key. (Unicode)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHEnumValue", "SHEnumValue function [Windows Shell]", "SHEnumValueW", "_win32_SHEnumValue", "shell.SHEnumValue", "shlwapi/SHEnumValue", "shlwapi/SHEnumValueW"]
old-location: shell\SHEnumValue.htm
tech.root: shell
ms.assetid: bb0eaa07-5112-4ce3-8796-5439bd863226
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHEnumValue, SHEnumValue function [Windows Shell], SHEnumValueA, SHEnumValueW, _win32_SHEnumValue, shell.SHEnumValue, shlwapi/SHEnumValue, shlwapi/SHEnumValueA, shlwapi/SHEnumValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHEnumValueW (Unicode) and SHEnumValueA (ANSI)
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
 - SHEnumValueW
 - shlwapi/SHEnumValueW
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
 - SHEnumValue
 - SHEnumValueA
 - SHEnumValueW
---

# SHEnumValueW function


## -description

Enumerates the values of the specified open registry key.

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

### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the value to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.

### -param pszValueName

Type: <b>LPTSTR</b>

The address of a character buffer that receives the enumerated value name. The size of this buffer is specified in <i>pcchValueName</i>.

### -param pcchValueName [in, out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pszValueName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszValueName</i>.

### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the data type of the value. These are the same values as those described under the <i>lpType</i> parameter of <a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>.

### -param pvData

Type: <b>LPVOID</b>

The address of a buffer that receives the data for the value entry. The size of this buffer is specified in <i>pcbData</i>. This parameter can be <b>NULL</b> if the data is not required.

### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pvData</i>, in bytes. On exit, this contains the number of bytes that were copied to <i>pvData</i>.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHEnumValue as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
