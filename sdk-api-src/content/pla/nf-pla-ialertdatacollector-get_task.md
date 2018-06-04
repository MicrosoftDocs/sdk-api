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

# IAlertDataCollector::get_Task


## -description


Retrieves or sets the name of a Task Scheduler job to start each time the counter value crosses the threshold. 

This property is read/write.


## -parameters


## -remarks



To specify command-line arguments for the task, see the <a href="https://msdn.microsoft.com/3062688f-a612-4824-beae-b75687b4feed">IAlertDataCollector::TaskArguments</a> and <a href="https://msdn.microsoft.com/d432652a-3dea-43f0-a698-bb7ccb1cb79a">IAlertDataCollector::TaskUserTextArguments</a> properties. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).




## -see-also




<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
 

 

