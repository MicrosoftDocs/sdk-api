---
UID: NF:shlwapi.StrRChrIA
title: StrRChrIA function
author: windows-sdk-content
description: Searches a string for the last occurrence of a specified character. The comparison is not case-sensitive.
old-location: shell\StrRChrI.htm
old-project: shell
ms.assetid: 3dc39c2a-d621-4f46-b65b-eb8a531e5abe
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: StrRChrI, StrRChrI function [Windows Shell], StrRChrIA, StrRChrIW, shell.StrRChrI, shlwapi/StrRChrI, shlwapi/StrRChrIA, shlwapi/StrRChrIW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrRChrIW (Unicode) and StrRChrIA (ANSI)
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
 - StrRChrI
 - StrRChrIA
 - StrRChrIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrRChrIA function


## -description


Searches a string for the last occurrence of a specified character. The comparison is not case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be searched.


### -param pszEnd [in, optional]

Type: <b>PCTSTR</b>

A pointer into the source string that defines the range of the search. Set <i>pszEnd</i> to point to a character in the string and the search will stop with the preceding character. Set <i>pszEnd</i> to <b>NULL</b> to search the entire string.


### -param wMatch

Type: <b>TCHAR</b>

The character to search for.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the last occurrence of the character in the string, if successful, or <b>NULL</b> if not.




## -remarks



The comparison assumes that <i>pszEnd</i> points to the end of the string.



