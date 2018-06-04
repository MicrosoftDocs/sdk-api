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

# StrCmpICA function


## -description


Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive.


## -parameters




### -param pszStr1

TBD


### -param pszStr2

TBD




#### - lpStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to the first null-terminated string to be compared.


#### - lpStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to the second null-terminated string to be compared.


## -returns



Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the string pointed to by <i>lpStr1</i> is alphabetically greater than that pointed to by <i>lpStr2</i>. Returns a negative value if the string pointed to by <i>lpStr1</i> is alphabetically less than that pointed to by <i>lpStr2</i>




## -remarks



It is strongly recommended that you use <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> in place of this function. <b>StrCmpIC</b> was designed for comparing canonical strings. These strings are not localized and consist only of characters below ASCII value 128. Therefore, it will not function correctly with double-byte character set (DBCS) data.

Uppercase characters are converted to lowercase characters before comparing, and the return value is based on comparing the converted values.  This function returns the difference in value of the first unequal characters it encounters, or zero if they are all equal. For example, if <i>lpStr1</i>="abczb" and <i>lpStr2</i>="abcdefg", <b>StrCmpIC</b> determines that "abczb" is greater than "abcdefg" and returns z - d.

For those versions of Windows that do not include <b>StrCmpIC</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>StrCmpICA</b> is ordinal 157 and <b>StrCmpICW</b> is ordinal 158.




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>
 

 

