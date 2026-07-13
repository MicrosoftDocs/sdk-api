---
UID: NF:shlwapi.SHRegQueryInfoUSKeyW
title: SHRegQueryInfoUSKeyW function (shlwapi.h)
description: Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["SHRegQueryInfoUSKey", "SHRegQueryInfoUSKey function [Windows Shell]", "SHRegQueryInfoUSKeyW", "_win32_SHRegQueryInfoUSKey", "shell.SHRegQueryInfoUSKey", "shlwapi/SHRegQueryInfoUSKey", "shlwapi/SHRegQueryInfoUSKeyW"]
old-location: shell\SHRegQueryInfoUSKey.htm
tech.root: shell
ms.assetid: e47b4fad-50c7-43d7-82f2-6a835ac543f0
ms.date: 12/05/2018
ms.keywords: SHRegQueryInfoUSKey, SHRegQueryInfoUSKey function [Windows Shell], SHRegQueryInfoUSKeyA, SHRegQueryInfoUSKeyW, _win32_SHRegQueryInfoUSKey, shell.SHRegQueryInfoUSKey, shlwapi/SHRegQueryInfoUSKey, shlwapi/SHRegQueryInfoUSKeyA, shlwapi/SHRegQueryInfoUSKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegQueryInfoUSKeyW (Unicode) and SHRegQueryInfoUSKeyA (ANSI)
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
 - SHRegQueryInfoUSKeyW
 - shlwapi/SHRegQueryInfoUSKeyW
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
 - SHRegQueryInfoUSKey
 - SHRegQueryInfoUSKeyA
 - SHRegQueryInfoUSKeyW
---

# SHRegQueryInfoUSKeyW function


## -description

Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

### -param pcSubKeys [out, optional]

Type: <b>LPDWORD</b>

A pointer to  a <b>DWORD</b> that receives the number of subkeys under the specified key.

### -param pcchMaxSubKeyLen [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the number of characters in the largest subkey name.

### -param pcValues [out, optional]

Type: <b>LPDWORD</b>

A pointer to  a <b>DWORD</b> that receives the number of values under the specified key.

### -param pcchMaxValueNameLen [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the number of characters in the largest value name.

### -param enumRegFlags [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a></b>

One of the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a> that specifies the base key in which the query should take place.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHRegQueryInfoUSKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
