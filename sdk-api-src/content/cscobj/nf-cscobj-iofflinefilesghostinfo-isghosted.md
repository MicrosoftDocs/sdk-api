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

# IOfflineFilesGhostInfo::IsGhosted


## -description


Determines whether the item is ghosted.


## -parameters




### -param pbGhosted [out]

Receives <b>TRUE</b> if the item is ghosted, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



An item is said to be ghosted in the offline files cache if, when the item is offline, its name is visible to the user, but its contents are not accessible. A file or directory can be in this state for one of the following reasons:

<ul>
<li>The item is pinned, which means that there is an entry for it in the cache.  However, either the content has not yet been synchronized to the client, or it was removed from the client (due to loss of oplock or detection of stale data) when the client transitioned offline.</li>
<li>The item has a sibling file or directory that is the root of a pinned namespace in the cache. When an item is pinned, its sibling items are ghosted so that the user can still see where the pinned item and its siblings are located in the online namespace even if the sibling items are not available offline.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/bb71bc95-049d-4ade-ad10-c33b0bf739ce">IOfflineFilesGhostInfo</a>



<a href="https://msdn.microsoft.com/9063a804-2597-4959-8249-e5b42f582ea3">IOfflineFilesPinInfo2::IsPartlyPinned</a>
 

 

