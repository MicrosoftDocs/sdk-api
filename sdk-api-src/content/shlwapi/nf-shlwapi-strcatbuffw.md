---
UID: NF:shlwapi.StrCatBuffW
title: StrCatBuffW function
author: windows-sdk-content
description: Copies and appends characters from one string to the end of another.
old-location: shell\StrCatBuff.htm
old-project: shell
ms.assetid: ce8c002f-f4f8-4b5f-a9e2-7bcd21f8808c
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: StrCatBuff, StrCatBuff function [Windows Shell], StrCatBuffA, StrCatBuffW, _win32_StrCatBuff, shell.StrCatBuff, shlwapi/StrCatBuff, shlwapi/StrCatBuffA, shlwapi/StrCatBuffW
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
req.unicode-ansi: StrCatBuffW (Unicode) and StrCatBuffA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
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
 - StrCatBuff
 - StrCatBuffA
 - StrCatBuffW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCatBuffW function


## -description


Copies and appends characters from one string to the end of another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param pszDest [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string. When this function returns successfully, this string contains its original content with the string <i>pszSrc</i> appended.


### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the string to be appended to <i>pszDest</i>.


### -param cchDestBuffSize

Type: <b>int</b>

The size of the buffer, in characters, pointed to by <i>pszDest</i>. This value must be at least the length of the combined string plus the terminating null character. If the buffer is too small to fit the entire string, the string will be truncated.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the destination string.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The final string is not guaranteed to be null-terminated. Consider using one of the following alternatives: <a href="https://msdn.microsoft.com/6330483b-dc61-4bbf-8ee7-e91a93495bb2">StringCbCat</a>, <a href="https://msdn.microsoft.com/db9f0731-0f7b-4018-ad07-1abe0bfe71e8">StringCbCatEx</a>, <a href="https://msdn.microsoft.com/56ef4ada-52df-48dd-a5e1-f62311be7592">StringCbCatN</a>, <a href="https://msdn.microsoft.com/ad1cad70-c548-4b2f-b253-b0af5000df08">StringCbCatNEx</a>, <a href="https://msdn.microsoft.com/72ddb6ab-8167-4213-815b-bd15b62d6123">StringCchCat</a>, <a href="https://msdn.microsoft.com/3b829dfa-6ede-47bd-b4d7-fcbf94a26c50">StringCchCatEx</a>, <a href="https://msdn.microsoft.com/516b67f9-ab6e-4c23-b04a-01848de09115">StringCchCatN</a>, or <a href="https://msdn.microsoft.com/63c9f437-b769-4c5a-9168-d0c458947abc">StringCchCatNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



