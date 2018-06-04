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

# IIdleSettings::get_RestartOnIdle


## -description


Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.

This property is read/write.


## -parameters


## -remarks



This property is only used if the <a href="https://msdn.microsoft.com/0799194f-dd3d-4aa6-b17b-0abe933f9b55">StopOnIdleEnd</a> property is set to True.

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/7a7a388c-8dc9-4106-82c1-3435d9f89866">RestartOnIdle</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

