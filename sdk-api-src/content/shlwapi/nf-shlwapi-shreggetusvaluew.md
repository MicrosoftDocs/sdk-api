---
UID: NF:shlwapi.SHRegGetUSValueW
title: SHRegGetUSValueW function (shlwapi.h)
description: Retrieves a value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["SHRegGetUSValue", "SHRegGetUSValue function [Windows Shell]", "SHRegGetUSValueW", "_win32_SHRegGetUSValue", "shell.SHRegGetUSValue", "shlwapi/SHRegGetUSValue", "shlwapi/SHRegGetUSValueW"]
old-location: shell\SHRegGetUSValue.htm
tech.root: shell
ms.assetid: 4d3b3bbe-dc2e-40c9-8ff1-0f9d2e323743
ms.date: 12/05/2018
ms.keywords: SHRegGetUSValue, SHRegGetUSValue function [Windows Shell], SHRegGetUSValueA, SHRegGetUSValueW, _win32_SHRegGetUSValue, shell.SHRegGetUSValue, shlwapi/SHRegGetUSValue, shlwapi/SHRegGetUSValueA, shlwapi/SHRegGetUSValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegGetUSValueW (Unicode) and SHRegGetUSValueA (ANSI)
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
 - SHRegGetUSValueW
 - shlwapi/SHRegGetUSValueW
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
 - SHRegGetUSValue
 - SHRegGetUSValueA
 - SHRegGetUSValueW
---

# SHRegGetUSValueW function


## -description

Retrieves a value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param pszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the subkey relative to <b>HKEY_LOCAL_MACHINE</b> and <b>HKEY_CURRENT_USER</b>. For example: "Software\MyCompany\MyProduct".

### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the value. This value can be <b>NULL</b>.

### -param pdwType [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> that receives the type of data stored in the retrieved value. When using default values, the input <i>pdwType</i> is the type of the default value. For possible values, see <a href="/windows/desktop/shell/hkey-type">Registry Data Types</a>. If type information is not required, this parameter can be <b>NULL</b>.

### -param pvData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that receives the value's data.

### -param pcbData [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by <i>pvData</i>. When <b>SHRegGetUSValue</b> returns, <i>pcbData</i> contains the size of the data copied to <i>pvData</i>.

### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

A variable that specifies which key to look under. When set to <b>TRUE</b>, <b>SHRegGetUSValue</b> ignores <b>HKEY_CURRENT_USER</b> and returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>.

### -param pvDefaultData [in, optional]

Type: <b>void*</b>

A pointer to a buffer that receives the value's default data.

### -param dwDefaultDataSize [in]

Type: <b>DWORD</b>

The length, in bytes, of the buffer pointed to by <i>pvDefaultData</i>.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

When <i>fIgnoreHKCU</i> is set to <b>TRUE</b>, <b>SHRegGetUSValue</b> returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>. When set to <b>FALSE</b>, <b>SHRegGetUSValue</b> first tries to return the value from the key under <b>HKEY_CURRENT_USER</b>. However, if the key is not found under <b>HKEY_CURRENT_USER</b>, the value is returned from the key under <b>HKEY_LOCAL_MACHINE</b>. If neither key is present, or if an error occurred and <i>dwDefaultDataSize</i> is nonzero, then the default data is copied to <i>pvData</i> and ERROR_SUCCESS returns. ERROR_SUCCESS returns for both default and non-default data, and there is no way of distinguishing which value copies to <i>pvData</i>. To prevent the use of default data, set <i>pvDefaultData</i> to <b>NULL</b> and <i>dwDefaultDataSize</i> to zero.

This function opens the key each time it is used. If your code involves getting a series of values from the same key, it is more efficient to open the key once with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> and then use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea">SHRegQueryUSValue</a> to retrieve the data.




> [!NOTE]
> The shlwapi.h header defines SHRegGetUSValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
