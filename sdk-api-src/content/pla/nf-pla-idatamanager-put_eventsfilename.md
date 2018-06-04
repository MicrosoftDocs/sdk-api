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

# IDataManager::put_EventsFileName


## -description


Retrieves or sets the name for the events file. 

This property is read/write.


## -parameters


## -remarks



PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="https://msdn.microsoft.com/e647987d-e524-475e-a355-539cb3f04635">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="https://msdn.microsoft.com/a1016784-8841-485f-885e-3719bdb0ae05">IDataManager::Run</a> method and if the data collection set contains trace data collectors.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

