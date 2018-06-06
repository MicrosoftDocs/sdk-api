---
UID: NF:shlwapi.IntlStrEqNA
title: IntlStrEqNA macro
author: windows-sdk-content
description: Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.
old-location: shell\IntlStrEqN.htm
old-project: shell
ms.assetid: ed777144-398c-4f36-bcc3-f6ba123ebfa7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IntlStrEqN, IntlStrEqN function [Windows Shell], IntlStrEqNA, IntlStrEqNW, _win32_IntlStrEqN, shell.IntlStrEqN, shlwapi/IntlStrEqN, shlwapi/IntlStrEqNA, shlwapi/IntlStrEqNW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IntlStrEqNW (Unicode) and IntlStrEqNA (ANSI)
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
api_name:
 - IntlStrEqN
 - IntlStrEqNA
 - IntlStrEqNW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IntlStrEqNA macro


## -description


Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.


## -parameters




### -param s1

TBD


### -param s2

TBD


### -param nChar [in]

Type: <b>int</b>

The number of characters to be compared, starting from the beginning of the strings.


#### - pszStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


#### - pszStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


## -remarks



This function retrieves the thread locale and uses <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> to do a case-sensitive comparison of the first <i>nChar</i> characters. It is equivalent to:
				

<pre class="syntax" xml:space="preserve"><code>IntlStrEqWorker(TRUE, pszStr1, pszStr2, nChar)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/bc8e823e-79b2-49fd-950d-96a6e7256377">IntlStrEqWorker</a>
 

 

