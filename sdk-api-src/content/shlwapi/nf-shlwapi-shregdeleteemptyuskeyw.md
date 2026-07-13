---
UID: NF:shlwapi.SHRegDeleteEmptyUSKeyW
title: SHRegDeleteEmptyUSKeyW function (shlwapi.h)
description: Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["SHRegDeleteEmptyUSKey", "SHRegDeleteEmptyUSKey function [Windows Shell]", "SHRegDeleteEmptyUSKeyW", "_win32_SHRegDeleteEmptyUSKey", "shell.SHRegDeleteEmptyUSKey", "shlwapi/SHRegDeleteEmptyUSKey", "shlwapi/SHRegDeleteEmptyUSKeyW"]
old-location: shell\SHRegDeleteEmptyUSKey.htm
tech.root: shell
ms.assetid: adb09a2b-674c-472d-9f16-8e150476f1f5
ms.date: 12/05/2018
ms.keywords: SHRegDeleteEmptyUSKey, SHRegDeleteEmptyUSKey function [Windows Shell], SHRegDeleteEmptyUSKeyA, SHRegDeleteEmptyUSKeyW, _win32_SHRegDeleteEmptyUSKey, shell.SHRegDeleteEmptyUSKey, shlwapi/SHRegDeleteEmptyUSKey, shlwapi/SHRegDeleteEmptyUSKeyA, shlwapi/SHRegDeleteEmptyUSKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegDeleteEmptyUSKeyW (Unicode) and SHRegDeleteEmptyUSKeyA (ANSI)
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
 - SHRegDeleteEmptyUSKeyW
 - shlwapi/SHRegDeleteEmptyUSKeyW
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
 - SHRegDeleteEmptyUSKey
 - SHRegDeleteEmptyUSKeyA
 - SHRegDeleteEmptyUSKeyW
---

# SHRegDeleteEmptyUSKeyW function


## -description

Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

### -param pwzSubKey

TBD

### -param delRegFlags [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregdel_flags">SHREGDEL_FLAGS</a></b>

One of the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregdel_flags">SHREGDEL_FLAGS</a> that specifies from which base key the subkey will be deleted.


#### - pszSubKey [in]

Type: <b>LPCSTR</b>

A pointer to  the null-terminated string that specifies the empty user-defined registry subkey to be deleted.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea">SHRegDeleteUSValue</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHRegDeleteEmptyUSKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
