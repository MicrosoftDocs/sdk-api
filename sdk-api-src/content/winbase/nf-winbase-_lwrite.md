---
UID: NF:winbase._lwrite
title: _lwrite function (winbase.h)
description: Writes data to the specified file.
helpviewer_keywords: ["_lwrite","_lwrite function [Windows API]","winbase/_lwrite","winprog._lwrite"]
old-location: winprog\_lwrite.htm
tech.root: winprog
ms.assetid: 34b875a4-ca45-4f9d-a5be-e6e4d41c68bf
ms.date: 12/05/2018
ms.keywords: _lwrite, _lwrite function [Windows API], winbase/_lwrite, winprog._lwrite
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _lwrite
 - winbase/_lwrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-private-l1-2-0.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-2.dll
api_name:
 - _lwrite
---

# _lwrite function


## -description

<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>WriteFile</b> function.]

Writes data to the specified file.

## -parameters

### -param hFile

A handle to the file that receives the data. This handle is created by <a href="/windows/win32/api/winbase/nf-winbase-_lcreat">_lcreat</a>.

### -param lpBuffer

The buffer that contains the data to be added.

### -param uBytes

The number of bytes to write to the file.

## -returns

If the function succeeds, the return value is the number of bytes written to the file. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>