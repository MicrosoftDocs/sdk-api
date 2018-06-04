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

# PathFindExtensionA function


## -description


Searches a path for an extension.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search, including the extension being searched for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the "." that precedes the extension within <i>pszPath</i> if an extension is found, or the address of the terminating null character otherwise.




## -remarks



Note that a valid file name extension cannot contain a space. For more information on valid file name extensions, see <a href="https://msdn.microsoft.com/c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50">File Type Handlers</a>.



