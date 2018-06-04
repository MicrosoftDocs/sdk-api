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

# IDataManager::get_ResourcePolicy


## -description


Retrieves or sets the action to take when one of the disk resource limits is exceeded. 

This property is read/write.


## -parameters


## -remarks



The folders are deleted based on the resource policy until the disk resource condition is satisfied. For example, if the maximum size is 7 MB and the current size is 10 MB, PLA will delete folders until the current size is 7 MB or less. If the first folder to be deleted is 3 MB, PLA will delete that folder and then stop deleting folders because the current size will be equal to the maximum size. If the first folder to be deleted is 9 MB, PLA will delete that folder and then stop deleting folders because the current size will be 1 MB, which will also satisfy the condition.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>



<a href="https://msdn.microsoft.com/59fad3d2-9971-4608-8576-977d4dd8ace4">IDataManager::FolderActions</a>
 

 

