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

# IOfflineFilesCache::RenameItem


## -description


Renames an item in the cache. This method logs a request with the Offline Files service for a path to be renamed on the next system restart.


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



This method requires system administrator privilege.

<div class="alert"><b>Note</b>  A restart of the system is necessary for the rename operation to be applied to the Offline Files cache.</div>
<div> </div>
This method fails if the path referenced by the <i>pszPathNew</i> parameter already exists in the Offline Files cache.

Beginning with Windows 8 and Windows Server 2012 you can also use the <a href="https://msdn.microsoft.com/766ABFE7-4417-47BA-ADF2-AA876C3A868A">IOfflineFilesCache2::RenameItemEx</a> method to rename an item. It does not require system administrator privilege or a system restart. However, it will fail if the item is currently in use.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>



<a href="https://msdn.microsoft.com/766ABFE7-4417-47BA-ADF2-AA876C3A868A">IOfflineFilesCache2::RenameItemEx</a>
 

 

