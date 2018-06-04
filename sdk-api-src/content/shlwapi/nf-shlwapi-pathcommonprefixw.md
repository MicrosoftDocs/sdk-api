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

# PathCommonPrefixW function


## -description


Compares two paths to determine if they share a common prefix. A prefix is one of these types: "C:\\", ".", "..", "..\\".


## -parameters




### -param pszFile1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the first path name.


### -param pszFile2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the second path name.


### -param achPath

TBD




#### - pszPath [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that receives the common prefix. This buffer must be at least MAX_PATH characters in size. If there is no common prefix, it is set to <b>NULL</b>.


## -returns



Type: <b>int</b>

Returns the count of common prefix characters in the path. If the output buffer pointer is not <b>NULL</b>, then these characters are copied to the output buffer.



