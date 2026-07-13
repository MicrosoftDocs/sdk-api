---
UID: NF:shlwapi.SHSetValueA
title: SHSetValueA function (shlwapi.h)
description: Sets the value of a registry key. (ANSI)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHSetValueA", "shlwapi/SHSetValueA"]
old-location: shell\SHSetValue.htm
tech.root: shell
ms.assetid: 6cd5b7fd-8fb9-4c24-9670-20c23ca709bf
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHSetValue, SHSetValue function [Windows Shell], SHSetValueA, SHSetValueW, _win32_SHSetValue, shell.SHSetValue, shlwapi/SHSetValue, shlwapi/SHSetValueA, shlwapi/SHSetValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHSetValueW (Unicode) and SHSetValueA (ANSI)
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
 - SHSetValueA
 - shlwapi/SHSetValueA
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
 - SHSetValue
 - SHSetValueA
 - SHSetValueW
---

# SHSetValueA function


## -description

Sets the value of a registry key.

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

The address of a null-terminated string that specifies the name of the subkey with which a value is associated. This can be <b>NULL</b> or a pointer to an empty string. In this case, the value is added to the key identified by the <i>hkey</i> parameter.

### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the value. This value can be <b>NULL</b>.

### -param dwType [in]

Type: <b>DWORD</b>

Type of data to be stored. This parameter must be the <b>REG_SZ</b> type. For more information, see <a href="/windows/desktop/shell/hkey-type">Registry Data Types</a>.

### -param pvData [in, optional]

Type: <b>LPCVOID</b>

Pointer to a buffer that contains the data to set for the specified value. This value can be <b>NULL</b>.

### -param cbData [in]

Type: <b>DWORD</b>

Length, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. If the data is a null-terminated string, this length includes the terminating null character.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful; otherwise, a nonzero error code defined in Winerror.h. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHSetValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
