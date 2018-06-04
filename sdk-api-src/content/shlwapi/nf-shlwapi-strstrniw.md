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

# StrStrNIW function


## -description


Finds the first occurrence of a substring within a string. The comparison is case-insensitive.


## -parameters




### -param pszFirst [in]

Type: <b>PWSTR</b>

A pointer to the null-terminated, Unicode string that is being searched.


### -param pszSrch [in]

Type: <b>PCWSTR</b>

A pointer to the null-terminated, Unicode substring that is being searched for.


### -param cchMax

Type: <b>UINT</b>

The maximum number of characters from the beginning of the searched string in which to search for the substring.


## -returns



Type: <b>PWSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.



