---
UID: NF:shlwapi.StrChrW
title: StrChrW function
author: windows-sdk-content
description: Searches a string for the first occurrence of a character that matches the specified character. The comparison is case-sensitive.
old-location: shell\StrChr.htm
tech.root: shell
ms.assetid: 3e4c20cb-0b46-4f84-bbd1-860fdedde8c8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: StrChr, StrChr function [Windows Shell], StrChrA, StrChrW, _win32_StrChr, shell.StrChr, shlwapi/StrChr, shlwapi/StrChrA, shlwapi/StrChrW
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
req.unicode-ansi: StrChrW (Unicode) and StrChrA (ANSI)
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
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrChr
 - StrChrA
 - StrChrW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrChrW function


## -description


Searches a string for the first occurrence of a character that matches the specified character. The comparison is case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PTSTR</b>

The address of the string to be searched.


### -param wMatch

Type: <b>TCHAR</b>

The character to be used for comparison.


## -returns



Type: <b>PTSTR</b>

Returns the address of the first occurrence of the character in the string if successful, or <b>NULL</b> otherwise.




## -remarks



The comparison assumes <i>pszStart</i> points to the start of a null-terminated string.



