---
UID: NF:winbase._lclose
title: "_lclose function"
author: windows-sdk-content
description: The _lclose function closes the specified file so that it is no longer available for reading or writing. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the CloseHandle function.
old-location: winprog\_lclose.htm
tech.root: devnotes
ms.assetid: FBFBD963-0461-4357-9362-D32A83C1F969
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "_lclose, _lclose function [Windows API], winbase/_lclose, winprog._lclose"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - iexpress.exe
 - wextract.exe
 - API-MS-Win-Core-Kernel32-Private-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-L1-1-2.dll
 - Kernel32Legacy.dll
api_name:
 - _lclose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _lclose function


## -description


The _lclose function closes the specified file so that it is no longer available for reading or writing. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the CloseHandle function.


## -parameters




### -param hFile

Identifies the file to be closed. This handle is returned by the function that created or last opened the file.


## -returns



Handle to file to close.



