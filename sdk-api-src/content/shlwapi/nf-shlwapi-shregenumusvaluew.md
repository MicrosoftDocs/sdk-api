---
UID: NF:shlwapi.SHRegEnumUSValueW
title: SHRegEnumUSValueW function (shlwapi.h)
description: Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["SHRegEnumUSValue", "SHRegEnumUSValue function [Windows Shell]", "SHRegEnumUSValueW", "_win32_SHRegEnumUSValue", "shell.SHRegEnumUSValue", "shlwapi/SHRegEnumUSValue", "shlwapi/SHRegEnumUSValueW"]
old-location: shell\SHRegEnumUSValue.htm
tech.root: shell
ms.assetid: 78ba5df4-8ee3-473f-b3ef-0bca65bb0a2a
ms.date: 12/05/2018
ms.keywords: SHRegEnumUSValue, SHRegEnumUSValue function [Windows Shell], SHRegEnumUSValueA, SHRegEnumUSValueW, _win32_SHRegEnumUSValue, shell.SHRegEnumUSValue, shlwapi/SHRegEnumUSValue, shlwapi/SHRegEnumUSValueA, shlwapi/SHRegEnumUSValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegEnumUSValueW (Unicode) and SHRegEnumUSValueA (ANSI)
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
 - SHRegEnumUSValueW
 - shlwapi/SHRegEnumUSValueW
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
api_name:
 - SHRegEnumUSValue
 - SHRegEnumUSValueA
 - SHRegEnumUSValueW
---

# SHRegEnumUSValueW function


## -description

Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSkey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the value to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.

### -param pszValueName [out]

Type: <b>LPTSTR</b>

A pointer to a character buffer that receives the enumerated value name. The size of this buffer is specified in <i>pcchValueNameLen</i>.

### -param pcchValueName [in, out]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pszValueName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszValueName</i>.

### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the data type of the value. These are the same values as those described under the <i>lpType</i> parameter of <a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>.

### -param pvData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that receives the data for the value entry. The size of this buffer is specified in <i>pcbData</i>. This parameter can be <b>NULL</b> if the data is not required.

### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pvData</i>. On exit, this contains the number of bytes that were copied to <i>pvData</i>.

### -param enumRegFlags [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a></b>

One of the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a> that specifies the base key in which the enumeration should take place.

## -returns

Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a textual description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHRegEnumUSValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
