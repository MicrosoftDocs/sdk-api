---
UID: NF:shlwapi.SHDeleteEmptyKeyA
title: SHDeleteEmptyKeyA function (shlwapi.h)
description: Deletes an empty key. (ANSI)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHDeleteEmptyKeyA", "shlwapi/SHDeleteEmptyKeyA"]
old-location: shell\SHDeleteEmptyKey.htm
tech.root: shell
ms.assetid: 6a560bc3-f65e-4b7d-9fbc-b4f2971ce2a9
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHDeleteEmptyKey, SHDeleteEmptyKey function [Windows Shell], SHDeleteEmptyKeyA, SHDeleteEmptyKeyW, _win32_SHDeleteEmptyKey, shell.SHDeleteEmptyKey, shlwapi/SHDeleteEmptyKey, shlwapi/SHDeleteEmptyKeyA, shlwapi/SHDeleteEmptyKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHDeleteEmptyKeyW (Unicode) and SHDeleteEmptyKeyA (ANSI)
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
 - SHDeleteEmptyKeyA
 - shlwapi/SHDeleteEmptyKeyA
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
 - SHDeleteEmptyKey
 - SHDeleteEmptyKeyA
 - SHDeleteEmptyKeyW
---

# SHDeleteEmptyKeyA function


## -description

Deletes an empty key.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

A handle to an open registry key, or one of the following <a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:

<a id="HKEY_CLASSES_ROOT"></a>
<a id="hkey_classes_root"></a>


#### HKEY_CLASSES_ROOT

<a id="HKEY_CURRENT_CONFIG"></a>
<a id="hkey_current_config"></a>


#### HKEY_CURRENT_CONFIG

<a id="HKEY_CURRENT_USER"></a>
<a id="hkey_current_user"></a>


#### HKEY_CURRENT_USER

<a id="HKEY_LOCAL_MACHINE"></a>
<a id="hkey_local_machine"></a>


#### HKEY_LOCAL_MACHINE

<a id="HKEY_PERFORMANCE_DATA"></a>
<a id="hkey_performance_data"></a>


#### HKEY_PERFORMANCE_DATA

<a id="HKEY_USERS"></a>
<a id="hkey_users"></a>


#### HKEY_USERS

### -param pszSubKey [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string specifying the name of the key to delete.

## -returns

Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a generic description of the error.

## -remarks

<b>SHDeleteEmptyKey</b> does not delete a key if it contains any subkeys or values. Use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya">SHDeleteKey</a> instead.

Alternatively, use the <a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regdeletetreea">RegDeleteTree</a> function.




> [!NOTE]
> The shlwapi.h header defines SHDeleteEmptyKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
