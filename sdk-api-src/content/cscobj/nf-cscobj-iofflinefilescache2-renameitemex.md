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

# IOfflineFilesCache2::RenameItemEx


## -description



    Renames an item in the cache. This method is identical to the <a href="https://msdn.microsoft.com/883f29cb-d551-4358-8e74-f901956d8829">IOfflineFilesCache::RenameItem</a> method, except that it will attempt to do the rename operation right away. 


## -parameters




### -param pszPathOriginal [in]

Fully qualified UNC path of the item (server, share, file or directory) to be renamed.


### -param pszPathNew [in]

The new path to replace <i>pszPathOriginal</i> if the item that  <i>pszPathOriginal</i> points to exists in the cache.


### -param bReplaceIfExists [in]

This parameter is reserved for future use.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method does not require system administrator privilege.

If the item to be renamed is a file or directory, it must obey the file system semantics for the rename operation. If the file or a child file (for a directory) is already open, the rename will fail. Also, this method attempts to perform the rename as long as the user has access to the item that is being renamed.

If you need to minimize the chance that the item is in use, call the <a href="https://msdn.microsoft.com/883f29cb-d551-4358-8e74-f901956d8829">IOfflineFilesCache::RenameItem</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/B4E2C2B0-AA6B-4657-8711-E5057720AF15">IOfflineFilesCache2</a>
 

 

