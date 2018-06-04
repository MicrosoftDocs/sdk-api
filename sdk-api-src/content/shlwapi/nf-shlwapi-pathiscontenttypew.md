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

# PathIsContentTypeW function


## -description


Determines if a file's registered content type matches the specified content type. This function obtains the content type for the specified file type and compares that string with the <i>pszContentType</i>. The comparison is not case-sensitive.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file whose content type will be compared.


### -param pszContentType [in]

Type: <b>LPCTSTR</b>

The address of a character buffer that contains the null-terminated content type string to which the file's registered content type will be compared.


## -returns



Type: <b>BOOL</b>

Returns nonzero if the file's registered content type matches <i>pszContentType</i>, or zero otherwise.



