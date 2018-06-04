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

# IntlStrEqWorkerW function


## -description


Compares a specified number of characters from the beginning of two localized strings.


## -parameters




### -param fCaseSens [in]

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> for a case-sensitive comparison, or to <b>FALSE</b> for a case-insensitive comparison.


### -param lpString1

TBD


### -param lpString2

TBD


### -param nChar [in]

Type: <b>int</b>

The number of characters to be compared, starting from the beginning of the strings.


#### - pszStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


#### - pszStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the first <i>nChar</i> characters are identical, or <b>FALSE</b> otherwise.




## -remarks



This function retrieves the thread locale and uses <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> to determine whether the first <i>nChar</i> characters are identical.



