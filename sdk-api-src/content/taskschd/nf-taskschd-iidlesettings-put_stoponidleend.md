---
UID: NF:taskschd.IIdleSettings.put_StopOnIdleEnd
title: IIdleSettings::put_StopOnIdleEnd (taskschd.h)
description: Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed. The idle condition ends when the computer is no longer idle.
helpviewer_keywords: ["IIdleSettings interface [Task Scheduler]","StopOnIdleEnd property","IIdleSettings.StopOnIdleEnd","IIdleSettings.put_StopOnIdleEnd","IIdleSettings::StopOnIdleEnd","IIdleSettings::get_StopOnIdleEnd","IIdleSettings::put_StopOnIdleEnd","StopOnIdleEnd property [Task Scheduler]","StopOnIdleEnd property [Task Scheduler]","IIdleSettings interface","put_StopOnIdleEnd","taskschd.iidlesettings_stoponidleend","taskschd/IIdleSettings::StopOnIdleEnd","taskschd/IIdleSettings::get_StopOnIdleEnd","taskschd/IIdleSettings::put_StopOnIdleEnd"]
old-location: taskschd\iidlesettings_stoponidleend.htm
tech.root: taskschd
ms.assetid: 0799194f-dd3d-4aa6-b17b-0abe933f9b55
ms.date: 12/05/2018
ms.keywords: IIdleSettings interface [Task Scheduler],StopOnIdleEnd property, IIdleSettings.StopOnIdleEnd, IIdleSettings.put_StopOnIdleEnd, IIdleSettings::StopOnIdleEnd, IIdleSettings::get_StopOnIdleEnd, IIdleSettings::put_StopOnIdleEnd, StopOnIdleEnd property [Task Scheduler], StopOnIdleEnd property [Task Scheduler],IIdleSettings interface, put_StopOnIdleEnd, taskschd.iidlesettings_stoponidleend, taskschd/IIdleSettings::StopOnIdleEnd, taskschd/IIdleSettings::get_StopOnIdleEnd, taskschd/IIdleSettings::put_StopOnIdleEnd
f1_keywords:
- taskschd/IIdleSettings.StopOnIdleEnd
dev_langs:
- c++
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
- IIdleSettings.StopOnIdleEnd
- IIdleSettings.get_StopOnIdleEnd
- IIdleSettings.put_StopOnIdleEnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdleSettings::put_StopOnIdleEnd


## -description


Gets or sets a Boolean value that  indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed. The idle condition ends when the computer is no longer idle.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-terminateonidleend-idlesettingstype-element">TerminateOnIdleEnd</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

