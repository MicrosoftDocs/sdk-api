---
UID: NF:shlwapi.StrCpyNW
title: StrCpyNW function
author: windows-sdk-content
description: Copies a specified number of characters from the beginning of one string to another.Note  Do not use this function or the StrNCpy macro.
old-location: shell\StrCpyN.htm
old-project: shell
ms.assetid: 7e21414d-0d82-40b9-b32f-5eaf351166da
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StrCpyN, StrCpyN function [Windows Shell], StrCpyNW, _win32_StrCpyN, shell.StrCpyN, shlwapi/StrCpyN, shlwapi/StrCpyNW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCpyNW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrCpyN
 - StrCpyNW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCpyNW function


## -description


Copies a specified number of characters from the beginning of one string to another.
<div class="alert"><b>Note</b>  Do not use this function or the <b>StrNCpy</b> macro. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param pszDst [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This buffer must be of sufficient size to hold the copied characters. This string is not guaranteed to be null-terminated.


### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.


### -param cchMax

Type: <b>int</b>

The number of characters to be copied, including the terminating null character.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>pszDst</i>.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated.  Consider using one of the following alternatives. <a href="https://msdn.microsoft.com/en-us/library/ms647499(v=VS.85).aspx">StringCbCopy</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647500(v=VS.85).aspx">StringCbCopyEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647501(v=VS.85).aspx">StringCbCopyN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647503(v=VS.85).aspx">StringCbCopyNEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647527(v=VS.85).aspx">StringCchCopy</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647529(v=VS.85).aspx">StringCchCopyEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647530(v=VS.85).aspx">StringCchCopyN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms647533(v=VS.85).aspx">StringCchCopyNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



