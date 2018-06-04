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

# StrCmpNCW function


## -description


Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is case-sensitive.


## -parameters




### -param pszStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to the first null-terminated string to be compared.


### -param pszStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to the second null-terminated string to be compared.


### -param nChar

Type: <b>int</b>

The number of characters from the beginning of each string to be compared.


## -returns



Type: <b>int</b>

Returns zero if the substrings are identical. Returns a positive value if the string taken from that pointed to by <i>pszStr1</i> is alphabetically greater than the string taken from that pointed to by <i>pszStr2</i>. Returns a negative value if the string taken from that pointed to by <i>pszStr1</i> is alphabetically less than the string taken from that pointed to by <i>pszStr2</i>.




## -remarks



Note that <b>StrCmpNC</b> was designed for comparing canonical strings. These strings are not localized and consist only of characters below ASCII value 128. Therefore, it will not function correctly with a double-byte character set (DBCS) or other multiple-character data.

This function locates the first unequal characters and returns a positive number if the character from the first string is greater than the character from the second, a negative number if it is less, or zero if they are equal. For example, suppose that <i>pszStr1</i>="abczb", <i>pszStr2</i>="abcdefg", and you are comparing the first four characters from each. <b>StrCmpNC</b> determines that the first unequal character is at position four ("z" in <i>pszStr1</i> and "d" in <i>pszStr2</i>) and returns a positive value since the ASCII code for "z" is greater than the ASCII code for "d".

For those versions of Windows that do not include <b>StrCmpNC</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>StrCmpNCA</b> is ordinal 151 and <b>StrCmpNCW</b> is ordinal 152.




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/f4c4bc76-1e42-4cb0-bf74-d395743c9b1c">StrCmpC</a>



<a href="https://msdn.microsoft.com/e2d97502-1819-463e-a56a-2d22b33502b7">StrCmpN</a>
 

 

