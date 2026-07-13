---
UID: NF:shlwapi.SHRegEnumUSKeyA
title: SHRegEnumUSKeyA function (shlwapi.h)
description: Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (ANSI)
helpviewer_keywords: ["SHRegEnumUSKeyA", "shlwapi/SHRegEnumUSKeyA"]
old-location: shell\SHRegEnumUSKey.htm
tech.root: shell
ms.assetid: 9418ad45-f451-4976-afd7-fa1e0088038d
ms.date: 12/05/2018
ms.keywords: SHRegEnumUSKey, SHRegEnumUSKey function [Windows Shell], SHRegEnumUSKeyA, SHRegEnumUSKeyW, _win32_SHRegEnumUSKey, shell.SHRegEnumUSKey, shlwapi/SHRegEnumUSKey, shlwapi/SHRegEnumUSKeyA, shlwapi/SHRegEnumUSKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegEnumUSKeyW (Unicode) and SHRegEnumUSKeyA (ANSI)
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
 - SHRegEnumUSKeyA
 - shlwapi/SHRegEnumUSKeyA
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
 - SHRegEnumUSKey
 - SHRegEnumUSKeyA
 - SHRegEnumUSKeyW
---

# SHRegEnumUSKeyA function


## -description

Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the subkey to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.

### -param pszName [out]

Type: <b>LPTSTR</b>

A pointer to a character buffer that receives the enumerated key name.

### -param pcchName [in, out]

Type: <b>LPDWORD</b>

A pointer to  a DWORD that, on entry, contains the size of the buffer at <i>pszName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszName</i>.

### -param enumRegFlags [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a></b>

A <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregenum_flags">SHREGENUM_FLAGS</a> that specifies the base key in which the enumeration should take place.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHRegEnumUSKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
