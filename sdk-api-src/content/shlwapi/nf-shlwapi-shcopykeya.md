---
UID: NF:shlwapi.SHCopyKeyA
title: SHCopyKeyA function (shlwapi.h)
description: Recursively copies the subkeys and values of the source subkey to the destination key. SHCopyKey does not copy the security attributes of the keys. (ANSI)
helpviewer_keywords: ["SHCopyKeyA", "shlwapi/SHCopyKeyA"]
old-location: shell\SHCopyKey.htm
tech.root: shell
ms.assetid: 52521ef4-fe59-4766-8828-acb557b0e968
ms.date: 12/05/2018
ms.keywords: SHCopyKey, SHCopyKey function [Windows Shell], SHCopyKeyA, SHCopyKeyW, _win32_SHCopyKey, shell.SHCopyKey, shlwapi/SHCopyKey, shlwapi/SHCopyKeyA, shlwapi/SHCopyKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHCopyKeyW (Unicode) and SHCopyKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCopyKeyA
 - shlwapi/SHCopyKeyA
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
 - SHCopyKey
 - SHCopyKeyA
 - SHCopyKeyW
---

# SHCopyKeyA function


## -description

Recursively copies the subkeys and values of the source subkey to the destination key. <b>SHCopyKey</b> does not copy the security attributes of the keys.

## -parameters

### -param hkeySrc [in]

Type: <b>HKEY</b>

A handle to the source key (for example, <b>HKEY_CURRENT_USER</b>).

### -param pszSrcSubKey [in, optional]

Type: <b>LPCTSTR</b>

The subkey whose subkeys and values are to be copied.

### -param hkeyDest [in]

Type: <b>HKEY</b>

The destination key.

### -param fReserved

Type: <b>DWORD</b>

Reserved. Must be 0.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or one of the nonzero error codes defined in Winerror.h otherwise. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.

## -remarks

<div class="alert"><b>Important</b>  This function does not duplicate the security attributes of the keys and values that it copies. Rather, all security attributes in the destination key are the default attributes.</div>
<div> </div>



> [!NOTE]
> The shlwapi.h header defines SHCopyKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
