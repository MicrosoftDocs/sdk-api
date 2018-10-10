---
UID: NF:shlwapi.StrNCatA
title: StrNCatA function
author: windows-sdk-content
description: Appends a specified number of characters from the beginning of one string to the end of another.
old-location: shell\StrNCat.htm
tech.root: shell
ms.assetid: 28099350-5759-4595-8353-3452c5cf6ca8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: StrNCat, StrNCat function [Windows Shell], StrNCatA, StrNCatW, _win32_StrNCat, shell.StrNCat, shlwapi/StrNCat, shlwapi/StrNCatA, shlwapi/StrNCatW
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
req.unicode-ansi: StrNCatW (Unicode) and StrNCatA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrNCat
 - StrNCatA
 - StrNCatW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrNCatA function


## -description


Appends a specified number of characters from the beginning of one string to the end of another.
            
            
<div class="alert"><b>Note</b>  Do not use this function or the <b>StrCatN</b> macro. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param psz1 [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string to which the function appends the characters from <i>psz2</i>. It must be large enough to hold the combined strings plus the terminating null character.


### -param psz2

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be appended.


### -param cchMax

Type: <b>int</b>

The number of characters to be appended to <i>psz1</i> from the beginning of <i>psz2</i>.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>, which holds the combined string.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Be aware that the last argument, <i>cchMax</i>, is the number of characters to copy into <i>psz1</i>, not necessarily the size of the <i>psz1</i> in bytes. Consider using one of the following alternatives. <a href="https://msdn.microsoft.com/en-us/library/ms647495(v=VS.85).aspx">StringCbCat</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647496(v=VS.85).aspx">StringCbCatEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647497(v=VS.85).aspx">StringCbCatN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647498(v=VS.85).aspx">StringCbCatNEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647518(v=VS.85).aspx">StringCchCat</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647520(v=VS.85).aspx">StringCchCatEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647522(v=VS.85).aspx">StringCchCatN</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms647524(v=VS.85).aspx">StringCchCatNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



