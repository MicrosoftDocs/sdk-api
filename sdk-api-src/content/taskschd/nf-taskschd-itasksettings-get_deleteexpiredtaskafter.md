---
UID: NF:taskschd.ITaskSettings.get_DeleteExpiredTaskAfter
title: ITaskSettings::get_DeleteExpiredTaskAfter
author: windows-sdk-content
description: Gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.
old-location: taskschd\itasksettings_deleteexpiredtaskafter.htm
tech.root: taskschd
ms.assetid: c6a2a12d-a41a-4fd8-a328-bce0fe19deba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteExpiredTaskAfter property [Task Scheduler], DeleteExpiredTaskAfter property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],DeleteExpiredTaskAfter property, ITaskSettings.DeleteExpiredTaskAfter, ITaskSettings.get_DeleteExpiredTaskAfter, ITaskSettings::DeleteExpiredTaskAfter, ITaskSettings::get_DeleteExpiredTaskAfter, ITaskSettings::put_DeleteExpiredTaskAfter, get_DeleteExpiredTaskAfter, taskschd.itasksettings_deleteexpiredtaskafter, taskschd/ITaskSettings::DeleteExpiredTaskAfter, taskschd/ITaskSettings::get_DeleteExpiredTaskAfter, taskschd/ITaskSettings::put_DeleteExpiredTaskAfter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.DeleteExpiredTaskAfter
 - ITaskSettings.get_DeleteExpiredTaskAfter
 - ITaskSettings.put_DeleteExpiredTaskAfter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskSettings::get_DeleteExpiredTaskAfter


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
 

 

