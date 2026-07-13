---
UID: NF:securitybaseapi.SetCachedSigningLevel
tech.root: security
title: SetCachedSigningLevel (securitybaseapi.h)
ms.date: 04/10/2023
targetos: Windows
description: Sets the cached signing level.
ms.keywords: SetCachedSigningLevel
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: securitybaseapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-security-base-l1-2-1.dll
 - api-ms-win-security-base-l1-2-0.dll
 - securitybaseapi.h
api_name:
 - SetCachedSigningLevel
f1_keywords:
 - SetCachedSigningLevel
 - securitybaseapi/SetCachedSigningLevel
dev_langs:
 - c++
helpviewer_keywords:
 - SetCachedSigningLevel
---

# SetCachedSigningLevel function (securitybaseapi.h)

## -description

Sets the cached signing level.

## -parameters

### -param SourceFiles [in]

Pointer to a set of source file handles.

### -param SourceFileCount [in]

The source file count.

### -param Flags [in]

The flags set for the file. The following *Flags* are supported:

| Flag | Value |
|--------|--------|
| **SIGNING_LEVEL_FILE_CACHE_FLAG_NOT_VALIDATED** | `0x01` |
| **SIGNING_LEVEL_FILE_CACHE_FLAG_VALIDATE_ONLY** | `0x04` |

Using these flags together (**SIGNING_LEVEL_FILE_CACHE_FLAG_NOT_VALIDATED \| SIGNING_LEVEL_FILE_CACHE_FLAG_VALIDATE_ONLY**) indicates that the file should be validated.

### -param TargetFile [in, optional]

The target file.

## -returns

If the function succeeds, it returns **TRUE**.

If the function fails, it returns **FALSE**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** may return one of the error codes defined in WinError.h.

## -remarks

## -see-also

[GetCachedSigningLevel](nf-securitybaseapi-getcachedsigninglevel.md)
