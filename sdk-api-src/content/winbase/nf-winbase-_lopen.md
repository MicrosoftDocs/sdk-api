---
UID: NF:winbase._lopen
title: _lopen function (winbase.h)
description: The _lopen function opens an existing file and sets the file pointer to the beginning of the file. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the CreateFile function.
helpviewer_keywords: ["_lopen","_lopen function [Windows API]","winbase/_lopen","winprog._lopen"]
old-location: winprog\_lopen.htm
tech.root: winprog
ms.assetid: E920F688-C694-44A6-ABD3-5414C4F01839
ms.date: 12/05/2018
ms.keywords: _lopen, _lopen function [Windows API], winbase/_lopen, winprog._lopen
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
 - _lopen
 - winbase/_lopen
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
 - wextract.exe
 - API-MS-Win-Core-Kernel32-Private-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-2.dll
 - Kernel32Legacy.dll
api_name:
 - _lopen
---

# _lopen function


## -description

The _lopen function opens an existing file and sets the file pointer to the beginning of the file. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the CreateFile function.

## -parameters

### -param lpPathName

Pointer to a null-terminated string that names the file to open. The string must consist of characters from the Windows ANSI character set.

### -param iReadWrite

Specifies the modes in which to open the file. This parameter consists of one access mode and an optional share mode. The access mode must be one of the following values: OF_READ,  OF_READWRITE, OF_WRITE

The share mode can be one of the following values: OF_SHARE_COMPAT,  OF_SHARE_DENY_NONE, OF_SHARE_DENY_READ, OF_SHARE_DENY_WRITE, OF_SHARE_EXCLUSIVE

## -returns

If the function succeeds, the return value is a file handle.

