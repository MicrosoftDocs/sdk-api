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

# StrChrNIW function


## -description


Searches a string for the first occurrence of a specified character. The comparison is not case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PCWSTR</b>

A pointer to the string to be searched.


### -param wMatch

Type: <b>WCHAR</b>

The character to be used for comparison.


### -param cchMax

Type: <b>UINT</b>

The maximum number of characters to search.


## -returns



Type: <b>PWSTR</b>

Returns the address of the first occurrence of the character in the string if successful, or <b>NULL</b> otherwise.




## -remarks



<b>StrChrNIW</b> searches for <i>wMatch</i> from <i>pszStart</i> to <i>pszStart</i> + <i>cchMax</i>, or until a <b>NULL</b> character is encountered.

To help ensure optimal performance, <i>pszStart</i> should be word-aligned.




## -see-also




<a href="https://msdn.microsoft.com/3e4c20cb-0b46-4f84-bbd1-860fdedde8c8">StrChr</a>



<a href="https://msdn.microsoft.com/bad606d2-e337-42b5-853e-c7afa8d3d71b">StrChrI</a>
 

 

