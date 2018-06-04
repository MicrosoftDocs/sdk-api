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

# PathIsSlowA function


## -description


<p class="CCE_Message">[<b>PathIsSlow</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a file path is a high-latency network connection.


## -parameters




### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the fully qualified path of the file.


### -param dwAttr

TBD




#### - dwFileAttr

Type: <b>DWORD</b>

The file attributes, if known; otherwise, pass –1 and this function gets the attributes by calling <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>. See <b>GetFileAttributes</b> for a list of file attributes.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the connection is high-latency; otherwise, <b>FALSE</b>.




## -remarks



A path is considered slow if the MultinetGetConnectionPerformance function returns a dwSpeed of 400 or less in its <a href="https://msdn.microsoft.com/977c717d-7624-46ab-b17d-25f42ef68be8">NETCONNECTINFOSTRUCT</a> structure—this is the speed of the media to the network resource, in 100 bits-per-second (bps)—or if FILE_ATTRIBUTE_OFFLINE is set on the file.

Note that network conditions can impact function performance time.



