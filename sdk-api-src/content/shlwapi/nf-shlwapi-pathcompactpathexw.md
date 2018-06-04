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

# PathCompactPathExW function


## -description


Truncates a path to fit within a certain number of characters by replacing path components with ellipses.


## -parameters




### -param pszOut [out]

Type: <b>LPTSTR</b>

The address of the string that has been altered.


### -param pszSrc [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be altered.


### -param cchMax [in]

Type: <b>UINT</b>

The maximum number of characters to be contained in the new string, including the terminating null character. For example, if <i>cchMax</i> = 8, the resulting string can contain a maximum of 7 characters plus the terminating null character.


### -param dwFlags [in]

Type: <b>DWORD</b>


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The '/' separator will be used instead of '\' if the original string used it. If <i>pszSrc</i> points to a file name that is too long, instead of a path, the file name will be truncated to <i>cchMax</i> characters, including the ellipsis and the terminating <b>NULL</b> character. For example, if the input file name is "My Filename" and <i>cchMax</i> is 10, <b>PathCompactPathEx</b> will return "My Fil...".



