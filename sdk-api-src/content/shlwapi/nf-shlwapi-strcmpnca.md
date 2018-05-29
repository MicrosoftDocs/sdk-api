---
UID: NF:shlwapi.StrCmpNCA
title: StrCmpNCA function
author: windows-sdk-content
description: Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is case-sensitive.
old-location: shell\StrCmpNC.htm
old-project: shell
ms.assetid: 4b4f18d3-9325-4bd9-ac65-af7f3012fdaa
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: StrCmpNC, StrCmpNC function [Windows Shell], StrCmpNCA, StrCmpNCW, _shell_StrCmpNC, shell.StrCmpNC, shlwapi/StrCmpNC, shlwapi/StrCmpNCA, shlwapi/StrCmpNCW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpNCW (Unicode) and StrCmpNCA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	StrCmpNC
-	StrCmpNCA
-	StrCmpNCW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCmpNCA function


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
 

 

