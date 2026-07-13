---
UID: NF:shlwapi.SHRegQueryUSValueW
title: SHRegQueryUSValueW function (shlwapi.h)
description: Retrieves the type and data for a specified name associated with an open registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHRegQueryUSValue", "SHRegQueryUSValue function [Windows Shell]", "SHRegQueryUSValueW", "_win32_SHRegQueryUSValue", "shell.SHRegQueryUSValue", "shlwapi/SHRegQueryUSValue", "shlwapi/SHRegQueryUSValueW"]
old-location: shell\SHRegQueryUSValue.htm
tech.root: shell
ms.assetid: 302a51b5-9cf9-46e5-908c-df0d3c31c91c
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHRegQueryUSValue, SHRegQueryUSValue function [Windows Shell], SHRegQueryUSValueA, SHRegQueryUSValueW, _win32_SHRegQueryUSValue, shell.SHRegQueryUSValue, shlwapi/SHRegQueryUSValue, shlwapi/SHRegQueryUSValueA, shlwapi/SHRegQueryUSValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegQueryUSValueW (Unicode) and SHRegQueryUSValueA (ANSI)
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
 - SHRegQueryUSValueW
 - shlwapi/SHRegQueryUSValueW
dev_langs:
 - c++
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
 - SHRegQueryUSValue
 - SHRegQueryUSValueA
 - SHRegQueryUSValueW
---

# SHRegQueryUSValueW function


## -description

Retrieves the type and data for a specified name associated with an open registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey, or one of the following predefined values. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.



#### HKEY_CLASSES_ROOT



#### HKEY_CURRENT_CONFIG



#### HKEY_CURRENT_USER



#### HKEY_LOCAL_MACHINE



#### HKEY_PERFORMANCE_DATA



#### HKEY_USERS

### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

A pointer to the <b>null</b>-terminated string that contains the name of the value to be queried.

### -param pdwType [in, out, optional]

Type: <b>LPDWORD*</b>

A pointer to the variable that sets or receives the key's value type. For more information, see <a href="/windows/desktop/shell/hkey-type">Registry Data Types</a>. This parameter can be <b>NULL</b>.

### -param pvData [out, optional]

Type: <b>LPVOID*</b>

A pointer to the buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not required.

### -param pcbData [in, out]

Type: <b>LPDWORD*</b>

A pointer to  the variable that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, this variable contains the size of the data copied to <i>pvData</i>.

### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

The variable that specifies which key to look under. When set to <b>TRUE</b>, <b>SHRegQueryUSValue</b> ignores <b>HKEY_CURRENT_USER</b> and returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>.

### -param pvDefaultData [in, optional]

Type: <b>LPVOID*</b>

A pointer to the default data.

### -param dwDefaultDataSize [in, optional]

Type: <b>DWORD</b>

The length, in bytes, of the default data.


##### - hUSKey.HKEY_CLASSES_ROOT


##### - hUSKey.HKEY_CURRENT_CONFIG


##### - hUSKey.HKEY_CURRENT_USER


##### - hUSKey.HKEY_LOCAL_MACHINE


##### - hUSKey.HKEY_PERFORMANCE_DATA


##### - hUSKey.HKEY_USERS

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

When <i>fIgnoreHKCU</i> is set to <b>TRUE</b>, <b>SHRegQueryUSValue</b> returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>. When set to <b>FALSE</b>, <b>SHRegQueryUSValue</b> first tries to return the value from the key under <b>HKEY_CURRENT_USER</b>. However, if the key is not found under <b>HKEY_CURRENT_USER</b>, the value returns from the key under <b>HKEY_LOCAL_MACHINE</b>. If neither key is present, or if an error occurs and <i>dwDefaultDataSize</i> is nonzero, then the default data is copied to <i>pvData</i> and ERROR_SUCCESS returns. ERROR_SUCCESS returns for both default and non-default data, and there is no way of distinguishing which value copies to <i>pvData</i>. To prevent the use of default data, set <i>pvDefaultData</i> to <b>NULL</b> and <i>dwDefaultDataSize</i> to zero.

If you only need to read a single value, <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea">SHRegGetUSValue</a> will both open the key and return the value. To use <b>SHRegQueryUSValue</b>, you must first open the key with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a>. However, once the key is opened, you can use <b>SHRegQueryUSValue</b> as many times as necessary. If you need to retrieve more than one value from the same key, using multiple calls to <b>SHRegQueryUSValue</b> is usually more efficient than <b>SHRegGetUSValue</b>, as the key is only opened once.




> [!NOTE]
> The shlwapi.h header defines SHRegQueryUSValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
