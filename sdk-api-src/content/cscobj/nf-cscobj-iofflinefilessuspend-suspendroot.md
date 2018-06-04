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

# IOfflineFilesSuspend::SuspendRoot


## -description



    Suspend or release a share root or directory tree.  A suspended item  is always in the offline state and is excluded from automatic synchronization by Offline Files.


## -parameters




### -param bSuspend [in]

Specify <b>TRUE</b> to suspend, or <b>FALSE</b> to release.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



When a share root or directory tree is suspended, all directories and files contained in the share or directory or in any subfolders are suspended as well.  This means that both directories and files may be suspended. Note that a directory can be suspended directly (if it is the root of the share or directory tree) or indirectly (if it is one of the items contained in the share or directory tree).




## -see-also




<a href="https://msdn.microsoft.com/697018c4-7cce-480a-b078-993cdac32bf5">IOfflineFilesSuspend</a>
 

 

