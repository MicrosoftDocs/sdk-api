---
UID: NF:shlwapi.SHRegCreateUSKeyA
title: SHRegCreateUSKeyA function (shlwapi.h)
description: Creates or opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE). (ANSI)
helpviewer_keywords: ["SHREGSET_DEFAULT", "SHREGSET_FORCE_HKCU", "SHREGSET_FORCE_HKLM", "SHREGSET_HKCU", "SHREGSET_HKLM", "SHRegCreateUSKeyA", "shlwapi/SHRegCreateUSKeyA"]
old-location: shell\SHRegCreateUSKey.htm
tech.root: shell
ms.assetid: 10e3e31e-bff6-4260-95fa-2d750de16ab3
ms.date: 12/05/2018
ms.keywords: SHREGSET_DEFAULT, SHREGSET_FORCE_HKCU, SHREGSET_FORCE_HKLM, SHREGSET_HKCU, SHREGSET_HKLM, SHRegCreateUSKey, SHRegCreateUSKey function [Windows Shell], SHRegCreateUSKeyA, SHRegCreateUSKeyW, _win32_SHRegCreateUSKey, shell.SHRegCreateUSKey, shlwapi/SHRegCreateUSKey, shlwapi/SHRegCreateUSKeyA, shlwapi/SHRegCreateUSKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegCreateUSKeyW (Unicode) and SHRegCreateUSKeyA (ANSI)
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
 - SHRegCreateUSKeyA
 - shlwapi/SHRegCreateUSKeyA
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
 - SHRegCreateUSKey
 - SHRegCreateUSKeyA
 - SHRegCreateUSKeyW
---

# SHRegCreateUSKeyA function


## -description

Creates or opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the subkey to be created or opened. If a value with this name is already present in the subkey, it will be opened.

### -param samDesired [in]

Type: <b><a href="/windows/desktop/shell/messages">REGSAM</a></b>

The desired security access. For more information on security access, see <a href="/windows/desktop/shell/messages">REGSAM</a>.

### -param hRelativeUSKey [in, optional]

Type: <b>HUSKEY</b>

The key to be used as a base for relative paths. If <i>pszPath</i> is a relative path, the key it specifies will be relative to <i>hRelativeUSKey</i>. If <i>pszPath</i> is an absolute path, set <i>hRelativeUSKey</i> to <b>NULL</b>. The key will then be created under <b>HKEY_LOCAL_MACHINE</b> or <b>HKEY_CURRENT_USER</b>, depending the value of <i>dwFlags</i>.

### -param phNewUSKey [out]

Type: <b>PHUSKEY</b>

A pointer to an <b>HUSKEY</b> that will receive the handle to the new key.

### -param dwFlags [in]

Type: <b>DWORD</b>

The base key under which the key should be opened. This can be one or more of the following values.



#### SHREGSET_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Only creates a key if it is empty.



#### SHREGSET_FORCE_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Creates a key even if it is not empty.



#### SHREGSET_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Only creates a key if it is empty.



#### SHREGSET_FORCE_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Creates a key even if it is not empty.



#### SHREGSET_DEFAULT

Create/open the key under both <b>HKEY_CURRENT_USER</b> (forced) and <b>HKEY_LOCAL_MACHINE</b> (only if empty). This flag is the equivalent of (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

If you want to write values to the new key, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea">SHRegWriteUSValue</a> to write each value, passing the <b>HUSKEY</b> handle that is returned through <i>phNewUSKey</i>. When you have finished, close the user-specific registry key with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey">SHRegCloseUSKey</a>.




> [!NOTE]
> The shlwapi.h header defines SHRegCreateUSKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
