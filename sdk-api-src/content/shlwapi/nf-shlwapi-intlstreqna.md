---
UID: NF:shlwapi.IntlStrEqNA
title: IntlStrEqNA macro (shlwapi.h)
description: Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.
old-location: shell\IntlStrEqN.htm
tech.root: shell
ms.assetid: ed777144-398c-4f36-bcc3-f6ba123ebfa7
ms.date: 12/05/2018
ms.keywords: IntlStrEqN, IntlStrEqN function [Windows Shell], IntlStrEqNA, IntlStrEqNW, _win32_IntlStrEqN, shell.IntlStrEqN, shlwapi/IntlStrEqN, shlwapi/IntlStrEqNA, shlwapi/IntlStrEqNW
ms.topic: macro
f1_keywords:
- shlwapi/IntlStrEqN
dev_langs:
- c++
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
- IntlStrEqN
- IntlStrEqNA
- IntlStrEqNW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IntlStrEqNA macro


## -description


Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.


## -parameters




### -param s1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


### -param s2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


### -param nChar [in]

Type: <b>int</b>

The number of characters to be compared, starting from the beginning of the strings.


## -remarks



This function retrieves the thread locale and uses <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> to do a case-sensitive comparison of the first <i>nChar</i> characters. It is equivalent to:
				

<pre class="syntax" xml:space="preserve"><code>IntlStrEqWorker(TRUE, pszStr1, pszStr2, nChar)</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-intlstreqworkera">IntlStrEqWorker</a>
 

 

