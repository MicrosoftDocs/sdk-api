---
UID: NF:shlwapi.StrCmpICW
title: StrCmpICW function
author: windows-driver-content
description: Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive.
old-location: shell\StrCmpIC.htm
old-project: shell
ms.assetid: 3f6d1ca1-fbd2-4ce2-b6d4-c3dfb37f1f87
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: StrCmpIC, StrCmpIC function [Windows Shell], StrCmpICA, StrCmpICW, _shell_StrCmpIC, shell.StrCmpIC, shlwapi/StrCmpIC, shlwapi/StrCmpICA, shlwapi/StrCmpICW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpICW (Unicode) and StrCmpICA (ANSI)
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
-	StrCmpIC
-	StrCmpICA
-	StrCmpICW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCmpICW function


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
 

 

