---
UID: NF:shlwapi.SHStrDupA
title: SHStrDupA function
author: windows-sdk-content
description: Makes a copy of a string in newly allocated memory.
old-location: shell\SHStrDup.htm
old-project: shell
ms.assetid: 6f014fb4-7637-48a8-9bec-d3278c46a6d8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHStrDup, SHStrDup function [Windows Shell], SHStrDupA, SHStrDupW, _win32_SHStrDup, shell.SHStrDup, shlwapi/SHStrDup, shlwapi/SHStrDupA, shlwapi/SHStrDupW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHStrDupW (Unicode) and SHStrDupA (ANSI)
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
-	API-MS-Win-shlwapi-IE-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
-	ShCore.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
-	API-MS-Win-ShCore-Obsolete-l1-1-0.dll
api_name:
-	SHStrDup
-	SHStrDupA
-	SHStrDupW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHStrDupA function


## -description


Makes a copy of a string in newly allocated memory.


## -parameters




### -param psz

TBD


### -param ppwsz [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated Unicode string that contains the result. <b>SHStrDup</b> allocates memory for this string with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. You should free the string with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.

                    

In the case of failure, this value is NULL.


#### - pszSource [in]

Type: <b>LPCTSTR</b>

A pointer to the null-terminated string to be copied.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This function will take either Unicode or ANSI strings as input, but the copied string is always Unicode.

This function uses <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> to allocate memory for the copied string. You must free this memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/fa77f0b3-8a9b-4221-87e3-9aebff4409fb">StrDup</a>
 

 

