---
UID: NF:shlwapi.IntlStrEqNIA
title: IntlStrEqNIA macro
author: windows-sdk-content
description: Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.
old-location: shell\IntlStrEqNI.htm
old-project: shell
ms.assetid: 3d201726-b24a-4739-84fb-49b54d3f0f07
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IntlStrEqNI, IntlStrEqNI function [Windows Shell], IntlStrEqNIA, IntlStrEqNIW, _win32_IntlStrEqNI, shell.IntlStrEqNI, shlwapi/IntlStrEqNI, shlwapi/IntlStrEqNIA, shlwapi/IntlStrEqNIW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IntlStrEqNIW (Unicode) and IntlStrEqNIA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - IntlStrEqNI
 - IntlStrEqNIA
 - IntlStrEqNIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IntlStrEqNIA macro


## -description


Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.


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



This function retrieves the thread locale and uses <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> to do a case-insensitive comparison of the first <i>nChar</i> characters. It is equivalent to:

<pre class="syntax" xml:space="preserve"><code>IntlStrEqWorker(FALSE, pszStr1, pszStr2, nChar)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/bc8e823e-79b2-49fd-950d-96a6e7256377">IntlStrEqWorker</a>
 

 

