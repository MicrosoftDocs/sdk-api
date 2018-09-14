---
UID: NF:shlwapi.wvnsprintfW
title: wvnsprintfW function
author: windows-sdk-content
description: Takes a list of arguments and returns the values of the arguments as a printf-style formatted string.
old-location: shell\wvnsprintf.htm
tech.root: shell
ms.assetid: a2aaaa05-d61e-41e3-8e49-7c0da1a661f0
ms.author: windowssdkdev
ms.date: 09/13/2018
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
---

# wvnsprintfW function


## -description


Takes a list of arguments and returns the values of the arguments as a <a href="https://msdn.microsoft.com/en-us/library/Ff728755(v=VS.85).aspx">printf</a>-style formatted string.
            
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

A <a href="https://msdn.microsoft.com/en-us/library/Ff728755(v=VS.85).aspx">printf</a>-style format string. The %s format identifier should never be used in an unbounded form. To avoid potential buffer overruns, always specify a size; for instance "%32s".


### -param arglist [in]

Type: <b>va_list</b>

A pointer to a list of command-line parameters used to customize the output.


## -returns



Type: <b>int</b>

Returns the number of characters written to the buffer, excluding any terminating <b>NULL</b> characters. A negative value is returned if an error occurs.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated. Consider using one of the following alternatives. <a href="https://msdn.microsoft.com/en-us/library/ms647510(v=VS.85).aspx">StringCbPrintf</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647513(v=VS.85).aspx">StringCbPrintfEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647514(v=VS.85).aspx">StringCbVPrintf</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647516(v=VS.85).aspx">StringCbVPrintfEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647541(v=VS.85).aspx">StringCchPrintf</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647543(v=VS.85).aspx">StringCchPrintfEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647546(v=VS.85).aspx">StringCchVPrintf</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms647548(v=VS.85).aspx">StringCchVPrintfEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



