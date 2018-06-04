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

# IEnumOfflineFilesItems::Clone


## -description


Creates a new instance of the enumerator with the same enumeration state as the current one.


## -parameters




### -param ppenum [out]

Address of an <a href="https://msdn.microsoft.com/9bb1fa14-74d2-4c6f-b8ba-47c6e78d7a4f">IEnumOfflineFilesItems</a> pointer variable that receives the interface pointer of the new enumeration object.


## -returns



Returns <b>S_OK</b> if the enumerator is created successfully, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9bb1fa14-74d2-4c6f-b8ba-47c6e78d7a4f">IEnumOfflineFilesItems</a>
 

 

