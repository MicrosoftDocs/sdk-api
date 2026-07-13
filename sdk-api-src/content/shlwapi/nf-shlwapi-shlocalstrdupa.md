---
UID: NF:shlwapi.SHLocalStrDupA
title: SHLocalStrDupA function (shlwapi.h)
description: Makes a copy of a string in newly allocated memory. (SHLocalStrDupA)
helpviewer_keywords: ["SHLocalStrDupA", "shlwapi/SHLocalStrDupA"]
old-location: shell\SHLocalStrDup.htm
tech.root: shell
ms.assetid: 79da6160-b1b1-41c3-9b21-229aadf251dd
ms.date: 12/05/2018
ms.keywords: SHLocalStrDup, SHLocalStrDup function [Windows Shell], SHLocalStrDupA, SHLocalStrDupW, _shell_SHLocalStrDup, shell.SHLocalStrDup, shlwapi/SHLocalStrDup, shlwapi/SHLocalStrDupA, shlwapi/SHLocalStrDupW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHLocalStrDupW (Unicode) and SHLocalStrDupA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHLocalStrDupA
 - shlwapi/SHLocalStrDupA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SHLocalStrDup
 - SHLocalStrDupA
 - SHLocalStrDupW
---

# SHLocalStrDupA function


## -description

Makes a copy of a string in newly allocated memory.

## -parameters

### -param psz

Type: <b>PCTSTR</b>

A pointer to a null-terminated, Unicode string to be copied.

### -param ppsz [out, optional]

Type: <b>PTSTR*</b>

The address of a pointer to an allocated string that, when this function returns successfully, receives the result. <b>SHLocalStrDup</b> allocates memory for this string with <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>. You should free the string with <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHLocalStrDup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
