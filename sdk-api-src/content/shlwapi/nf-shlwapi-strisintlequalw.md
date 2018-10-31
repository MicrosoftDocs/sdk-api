---
UID: NF:shlwapi.StrIsIntlEqualW
title: StrIsIntlEqualW function
author: windows-sdk-content
description: Compares a specified number of characters from the beginning of two strings to determine if they are equal.
old-location: shell\StrIsIntlEqual.htm
tech.root: shell
ms.assetid: 02c66644-8aab-4ddd-a3ab-d52aeaa900a3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: StrIsIntlEqual, StrIsIntlEqual function [Windows Shell], StrIsIntlEqualA, StrIsIntlEqualW, _win32_StrIsIntlEqual, shell.StrIsIntlEqual, shlwapi/StrIsIntlEqual, shlwapi/StrIsIntlEqualA, shlwapi/StrIsIntlEqualW
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
req.unicode-ansi: StrIsIntlEqualW (Unicode) and StrIsIntlEqualA (ANSI)
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
 - StrIsIntlEqual
 - StrIsIntlEqualA
 - StrIsIntlEqualW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrIsIntlEqualW function


## -description


Compares a specified number of characters from the beginning of two strings to determine if they are equal.


## -parameters




### -param fCaseSens

Type: <b>BOOL</b>

The case sensitivity of the comparison. If this value is nonzero, the comparison is case-sensitive. If this value is zero, the comparison is not case-sensitive.


### -param pszString1 [in]

Type: <b>PCTSTR</b>

A pointer to the first null-terminated string to be compared.


### -param pszString2 [in]

Type: <b>PCTSTR</b>

A pointer to the second null-terminated string to be compared.


### -param nChar

Type: <b>int</b>

The number of characters from the beginning of each string to be compared.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the first <i>nChar</i> characters from the two strings are equal; otherwise, <b>FALSE</b>.




## -remarks



You can set case sensitivity with the <b>StrIntlEqN</b> and <b>StrIntlEqNI</b> macros. <b>StrIntlEqN</b> performs a case-sensitive comparison, and <b>StrIntlEqNI</b> performs a case-insensitive comparison.

The syntax of the two macros is:
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define StrIntlEqN(s1, s2, nChar) StrIsIntlEqual(TRUE, s1, s2, nChar)
#define StrIntlEqNI(s1, s2, nChar) StrIsIntlEqual(FALSE, s1, s2, nChar)</pre>
</td>
</tr>
</table></span></div>


