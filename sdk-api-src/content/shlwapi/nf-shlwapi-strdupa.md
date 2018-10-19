---
UID: NF:shlwapi.StrDupA
title: StrDupA function
author: windows-sdk-content
description: Duplicates a string.
old-location: shell\StrDup.htm
tech.root: shell
ms.assetid: fa77f0b3-8a9b-4221-87e3-9aebff4409fb
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: StrDup, StrDup function [Windows Shell], StrDupA, StrDupW, _win32_StrDup, shell.StrDup, shlwapi/StrDup, shlwapi/StrDupA, shlwapi/StrDupW
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
req.unicode-ansi: StrDupW (Unicode) and StrDupA (ANSI)
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
 - StrDup
 - StrDupA
 - StrDupW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrDupA function


## -description


Duplicates a string.


## -parameters




### -param pszSrch

Type: <b>PCTSTR</b>

A pointer to a constant <b>null</b>-terminated character string.


## -returns



Type: <b>PTSTR</b>

Returns the address of the string that was copied, or <b>NULL</b> if the string cannot be copied.




## -remarks



<b>StrDup</b> will allocate storage the size of the original string. If storage allocation is successful, the original string is copied to the duplicate string.

This function uses <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> to allocate storage space for the copy of the string. The calling application must free this memory by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function on the pointer returned by the call to <b>StrDup</b>.


#### Examples

This simple console application illustrates the use of <b>StrDup</b>.


```cpp
#include <windows.h>
#include <shlwapi.h>
#include <stdio.h>

void main(void)
{
   char buffer[] = "This is the buffer text";
   char *newstring;

   // Note: Never use an unbounded %s format specifier in printf.
   printf("Original: %25s\n", buffer);

   newstring = StrDup(buffer);
   if (newstring != NULL)
   {
       printf("Copy:     %25s\n", newstring);
       LocalFree(newstring);
   }
}

OUTPUT:
- - - - - - 
Original: This is the buffer text
Copy:     This is the buffer text
```




