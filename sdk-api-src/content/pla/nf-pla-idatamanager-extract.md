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

# IDataManager::Extract


## -description


Extracts the specified CAB file.


## -parameters




### -param CabFilename




### -param DestinationPath [in]

The path where you want to place the CAB file.


#### - CabFileName [in]

The name of the CAB file to extract.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>



<a href="https://msdn.microsoft.com/7e7672d9-9384-4365-aa4a-bf8dace050c2">IFolderAction::Actions</a>
 

 

