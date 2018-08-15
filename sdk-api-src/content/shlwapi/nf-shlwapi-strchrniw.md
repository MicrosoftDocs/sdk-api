---
UID: NF:shlwapi.StrChrNIW
title: StrChrNIW function
author: windows-sdk-content
description: Searches a string for the first occurrence of a specified character. The comparison is not case-sensitive.
old-location: shell\StrChrNIW.htm
old-project: shell
ms.assetid: 01F2CC10-F59A-45dd-8A18-7DC33BDD717F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StrChrNIW, StrChrNIW function [Windows Shell], shell.StrChrNIW, shlwapi/StrChrNIW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - StrChrNIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrChrNIW function


## -description


Searches a string for the first occurrence of a specified character. The comparison is not case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PCWSTR</b>

A pointer to the string to be searched.


### -param wMatch

Type: <b>WCHAR</b>

The character to be used for comparison.


### -param cchMax

Type: <b>UINT</b>

The maximum number of characters to search.


## -returns



Type: <b>PWSTR</b>

Returns the address of the first occurrence of the character in the string if successful, or <b>NULL</b> otherwise.




## -remarks



<b>StrChrNIW</b> searches for <i>wMatch</i> from <i>pszStart</i> to <i>pszStart</i> + <i>cchMax</i>, or until a <b>NULL</b> character is encountered.

To help ensure optimal performance, <i>pszStart</i> should be word-aligned.




## -see-also




<a href="https://msdn.microsoft.com/3e4c20cb-0b46-4f84-bbd1-860fdedde8c8">StrChr</a>



<a href="https://msdn.microsoft.com/bad606d2-e337-42b5-853e-c7afa8d3d71b">StrChrI</a>
 

 

