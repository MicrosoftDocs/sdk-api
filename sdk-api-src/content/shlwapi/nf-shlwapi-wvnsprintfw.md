---
UID: NF:shlwapi.wvnsprintfW
title: wvnsprintfW function
author: windows-sdk-content
description: Takes a list of arguments and returns the values of the arguments as a printf-style formatted string.
old-location: shell\wvnsprintf.htm
tech.root: shell
ms.assetid: a2aaaa05-d61e-41e3-8e49-7c0da1a661f0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_wvnsprintf, shell.wvnsprintf, shlwapi/wvnsprintf, shlwapi/wvnsprintfA, shlwapi/wvnsprintfW, wvnsprintf, wvnsprintf function [Windows Shell], wvnsprintfA, wvnsprintfW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wvnsprintfW (Unicode) and wvnsprintfA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - wvnsprintf
 - wvnsprintfA
 - wvnsprintfW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- wvnsprintfW
: 
---

# wvnsprintfW function


## -description


Takes a list of arguments and returns the values of the arguments as a <a href="77a854ae-5b48-4865-89f4-f2dc5cf80f52">printf</a>-style formatted string.
            
<div class="alert"><b>Note</b>  Do not use this function. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param pszDest [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the output string.


### -param cchDest [in]

Type: <b>int</b>

The maximum number of characters allowed in <i>pszDest</i>.


### -param pszFmt [in]

Type: <b>PCTSTR</b>

A <a href="77a854ae-5b48-4865-89f4-f2dc5cf80f52">printf</a>-style format string. The %s format identifier should never be used in an unbounded form. To avoid potential buffer overruns, always specify a size; for instance "%32s".


### -param arglist [in]

Type: <b>va_list</b>

A pointer to a list of command-line parameters used to customize the output.


## -returns



Type: <b>int</b>

Returns the number of characters written to the buffer, excluding any terminating <b>NULL</b> characters. A negative value is returned if an error occurs.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated. Consider using one of the following alternatives. <a href="https://msdn.microsoft.com/224c8840-06c6-4144-8f23-8705ac8ef887">StringCbPrintf</a>, <a href="https://msdn.microsoft.com/525e1fb5-9dfd-4ec2-a4af-9b9e198b6e17">StringCbPrintfEx</a>, <a href="https://msdn.microsoft.com/d6985910-65be-4b68-b410-026cef66c651">StringCbVPrintf</a>, <a href="https://msdn.microsoft.com/36f77c17-6244-4357-9361-a04118fcd820">StringCbVPrintfEx</a>, <a href="https://msdn.microsoft.com/9eaafe87-04da-4273-babb-b16d26bfdf70">StringCchPrintf</a>, <a href="https://msdn.microsoft.com/e3904cd0-fcb9-4b54-9895-513a95f4a6f7">StringCchPrintfEx</a>, <a href="https://msdn.microsoft.com/82cc5a7c-e4c5-4a88-9bb5-d3f02dc3d7f5">StringCchVPrintf</a>, or <a href="https://msdn.microsoft.com/07b4eb68-2b50-4c66-af1a-13cc57144e3a">StringCchVPrintfEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



