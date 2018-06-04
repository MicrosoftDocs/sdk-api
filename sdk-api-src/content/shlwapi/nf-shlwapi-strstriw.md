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

# StrStrIW function


## -description


Finds the first occurrence of a substring within a string. The comparison is not case-sensitive.


## -parameters




### -param pszFirst [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string being searched.


### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.



