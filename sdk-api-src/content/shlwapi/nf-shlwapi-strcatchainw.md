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

# StrCatChainW function


## -description


Concatenates two Unicode strings. Used when repeated concatenations to the same buffer are required.


## -parameters




### -param pszDst [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the null-terminated, Unicode string.


### -param cchDst

Type: <b>DWORD</b>

The size of the destination buffer, in characters. This buffer must be of sufficient size to hold both strings as well as a terminating null character. If the buffer is too small, the final string is truncated.


### -param ichAt

Type: <b>DWORD</b>

The offset into the destination buffer at which to begin the append action. If the string is not empty, set this value to -1 to have the current number of filled characters (not including the terminating null character) calculated for you.


### -param pszSrc [in]

Type: <b>PCWSTR</b>

A pointer to the null-terminated Unicode source string.


## -returns



Type: <b>DWORD</b>

Returns the offset of the null character after the last character added to <i>pszDst</i>.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The final string is not guaranteed to be null-terminated. Consider using one of the following alternatives: <a href="https://msdn.microsoft.com/db9f0731-0f7b-4018-ad07-1abe0bfe71e8">StringCbCatEx</a>, <a href="https://msdn.microsoft.com/ad1cad70-c548-4b2f-b253-b0af5000df08">StringCbCatNEx</a>, <a href="https://msdn.microsoft.com/3b829dfa-6ede-47bd-b4d7-fcbf94a26c50">StringCchCatEx</a>, or <a href="https://msdn.microsoft.com/63c9f437-b769-4c5a-9168-d0c458947abc">StringCchCatNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



