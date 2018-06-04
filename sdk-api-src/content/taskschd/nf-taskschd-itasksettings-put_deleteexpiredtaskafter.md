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

# ITaskSettings::put_DeleteExpiredTaskAfter


## -description


Gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires. If no value  is specified for this property, then the Task Scheduler service will not delete the task.

This property is read/write.


## -parameters


## -remarks



A task expires after the end boundary has been exceeded for all triggers associated with the task. The end boundary for a trigger is specified by the <a href="https://msdn.microsoft.com/985316de-eaba-478f-a53f-1bea2a0cc9c6">EndBoundary</a> property inherited by all trigger interfaces.

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/947a2fec-ceda-4726-aa1a-26fd1b258c1f">DeleteExpiredTaskAfter (settingsType)</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

