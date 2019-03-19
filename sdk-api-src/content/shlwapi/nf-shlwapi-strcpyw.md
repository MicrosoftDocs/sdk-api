---
UID: NF:shlwapi.StrCpyW
title: StrCpyW function (shlwapi.h)
author: windows-sdk-content
description: Copies one string to another.
old-location: shell\StrCpy.htm
tech.root: shell
ms.assetid: 83d1a8dc-fc43-4b06-b36c-c9c91d779d25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StrCpy, StrCpy function [Windows Shell], StrCpyW, _win32_StrCpy, shell.StrCpy, shlwapi/StrCpy, shlwapi/StrCpyW
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCpyW (Unicode)
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
 - StrCpy
 - StrCpyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrCpyW function


## -description


Copies one string to another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param psz1 [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This string is not guaranteed to be null-terminated.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Consider using one of the following alternatives: <a href="https://msdn.microsoft.com/en-us/library/ms647499(v=VS.85).aspx">StringCbCopy</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647500(v=VS.85).aspx">StringCbCopyEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647501(v=VS.85).aspx">StringCbCopyN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647503(v=VS.85).aspx">StringCbCopyNEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647527(v=VS.85).aspx">StringCchCopy</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647529(v=VS.85).aspx">StringCchCopyEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647530(v=VS.85).aspx">StringCchCopyN</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms647533(v=VS.85).aspx">StringCchCopyNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



