---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


