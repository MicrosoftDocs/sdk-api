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

# IOfflineFilesCache::EnumSettingObjects


## -description



    Creates an enumerator of instances of <a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>. This allows the caller to enumerate all of the available settings that affect the behavior of Offline Files.


## -parameters




### -param ppEnum [out]

On success, receives the address of an instance of <a href="https://msdn.microsoft.com/2d0e45d5-5559-4c2e-9c20-4e5b84b5fbbd">IEnumOfflineFilesSettings</a>.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A known setting may be retrieved by name using <a href="https://msdn.microsoft.com/17b6572d-f05e-4f0e-a247-89acd2963d6b">IOfflineFilesCache::GetSettingObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

