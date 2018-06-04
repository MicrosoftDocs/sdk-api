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

# DavInvalidateCache function


## -description


Invalidates the contents of the local cache for a remote file on a WebDAV server.


## -parameters




### -param URLName [in]

A pointer to a Unicode string that contains the name of a remote file on a WebDAV server. This name can be an HTTP path name (URL) or a UNC path name.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The  <b>DavInvalidateCache</b> function marks the contents of the locally cached file (for the specified URL) for deletion. If this function succeeds, the local file cache is no longer valid. This function fails if there are any handles opened against the file either by the same process or by a different process on the local computer.

If the item that is named in the <i>URLName</i> parameter is not present in the cache, <b>DavInvalidateCache</b> returns ERROR_SUCCESS without invalidating the cache.



