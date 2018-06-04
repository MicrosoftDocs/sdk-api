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

# IOfflineFilesCache::ProcessAdminPinPolicy


## -description


Causes Offline Files to process the "administratively assigned offline files" group policy.


## -parameters




### -param pPinProgress [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being pinned in the Offline Files cache.


### -param pUnpinProgress [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being unpinned from the Offline Files cache.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The "administratively assigned offline files" group policy provides a way for administrators to cause specific folders to be pinned by Offline Files for specific users by way of the Group Policy mechanism.  The primary client of this function is the Offline Files Group Policy extension.  In most deployments there is no need to call this function.  The Group Policy extension will do that for you.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

