---
UID: NF:shlwapi.SHRegDeleteUSValueW
title: SHRegDeleteUSValueW function (shlwapi.h)
description: Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (Unicode)
helpviewer_keywords: ["SHRegDeleteUSValue", "SHRegDeleteUSValue function [Windows Shell]", "SHRegDeleteUSValueW", "_win32_SHRegDeleteUSValue", "shell.SHRegDeleteUSValue", "shlwapi/SHRegDeleteUSValue", "shlwapi/SHRegDeleteUSValueW"]
old-location: shell\SHRegDeleteUSValue.htm
tech.root: shell
ms.assetid: f70407af-d8ee-4333-be32-01887d4add4c
ms.date: 12/05/2018
ms.keywords: SHRegDeleteUSValue, SHRegDeleteUSValue function [Windows Shell], SHRegDeleteUSValueA, SHRegDeleteUSValueW, _win32_SHRegDeleteUSValue, shell.SHRegDeleteUSValue, shlwapi/SHRegDeleteUSValue, shlwapi/SHRegDeleteUSValueA, shlwapi/SHRegDeleteUSValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegDeleteUSValueW (Unicode) and SHRegDeleteUSValueA (ANSI)
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
 - SHRegDeleteUSValueW
 - shlwapi/SHRegDeleteUSValueW
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
 - SHRegDeleteUSValue
 - SHRegDeleteUSValueA
 - SHRegDeleteUSValueW
---

# SHRegDeleteUSValueW function


## -description

Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

### -param pwzValue

TBD

### -param delRegFlags [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregdel_flags">SHREGDEL_FLAGS</a></b>

One of the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shregdel_flags">SHREGDEL_FLAGS</a> that specifies from which base key the value will be deleted.


#### - pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to the null-terminated string that names the value to remove.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya">SHRegDeleteEmptyUSKey</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHRegDeleteUSValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
