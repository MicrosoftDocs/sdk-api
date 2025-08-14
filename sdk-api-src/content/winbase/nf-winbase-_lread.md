---
UID: NF:winbase._lread
title: _lread function (winbase.h)
description: The _lread function reads data from the specified file. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the ReadFile function.
helpviewer_keywords: ["_lread","_lread function [Windows API]","winbase/_lread","winprog._lread"]
old-location: winprog\_lread.htm
tech.root: winprog
ms.assetid: A5374B2B-12EC-4130-8D21-1801D1D72524
ms.date: 12/05/2018
ms.keywords: _lread, _lread function [Windows API], winbase/_lread, winprog._lread
req.header: winbase.h
req.include-header: 
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
 - _lread
 - winbase/_lread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-private-l1-2-0.dll
 - kernel32.dll
 - iexpress.exe
 - API-MS-Win-Core-Kernel32-Private-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-2.dll
 - Kernel32Legacy.dll
api_name:
 - _lread
---

# _lread function


## -description

The _lread function reads data from the specified file. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the ReadFile function.

## -parameters

### -param hFile

Identifies the specified file.

### -param lpBuffer

Pointer to a buffer that contains the data read from the file.

### -param uBytes

Specifies the number of bytes to be read from the file.

## -returns

The return value indicates the number of bytes actually read from the file. If the number of bytes read is less than uBytes, the function has reached the end of file (EOF) before reading the specified number of bytes.

