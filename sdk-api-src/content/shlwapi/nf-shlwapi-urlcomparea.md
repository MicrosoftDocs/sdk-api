---
UID: NF:shlwapi.UrlCompareA
title: UrlCompareA function
author: windows-driver-content
description: Makes a case-sensitive comparison of two URL strings.
old-location: shell\UrlCompare.htm
old-project: shell
ms.assetid: d5c9e003-b85b-4f9f-b231-e3e4b71d4ce6
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: UrlCompare, UrlCompare function [Windows Shell], UrlCompareA, UrlCompareW, _win32_UrlCompare, shell.UrlCompare, shlwapi/UrlCompare, shlwapi/UrlCompareA, shlwapi/UrlCompareW
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
req.unicode-ansi: UrlCompareW (Unicode) and UrlCompareA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-url-l1-1-0.dll
-	KernelBase.dll
api_name:
-	UrlCompare
-	UrlCompareA
-	UrlCompareW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlCompareA function


## -description


Makes a case-sensitive comparison of two URL strings.


## -parameters




### -param psz1 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the first URL.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the second URL.


### -param fIgnoreSlash

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> to have <b>UrlCompare</b> ignore a trailing '/' character on either or both URLs.


## -returns



Type: <b>int</b>

Returns zero if the two strings are equal. The function will also return zero if <i>fIgnoreSlash</i> is set to <b>TRUE</b> and one of the strings has a trailing '\' character. The function returns a negative integer if the string pointed to by <i>psz1</i> is less than the string pointed to by <i>psz2</i>. Otherwise, it returns a positive integer.




## -remarks



For best results, you should first canonicalize the URLs with <a href="https://msdn.microsoft.com/70802745-0611-4d37-800e-b50d5ea23426">UrlCanonicalize</a>. Then, compare the canonicalized URLs with <b>UrlCompare</b>.




## -see-also




<a href="https://msdn.microsoft.com/12530a04-776c-4506-86d1-07e2c3569a36">StrCmp</a>
 

 

