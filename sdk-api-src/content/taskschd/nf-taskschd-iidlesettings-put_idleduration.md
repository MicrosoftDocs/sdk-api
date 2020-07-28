---
UID: NF:taskschd.IIdleSettings.put_IdleDuration
title: IIdleSettings::put_IdleDuration (taskschd.h)
description: Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.
helpviewer_keywords: ["IIdleSettings interface [Task Scheduler]","IdleDuration property","IIdleSettings.IdleDuration","IIdleSettings.put_IdleDuration","IIdleSettings::IdleDuration","IIdleSettings::get_IdleDuration","IIdleSettings::put_IdleDuration","IdleDuration property [Task Scheduler]","IdleDuration property [Task Scheduler]","IIdleSettings interface","put_IdleDuration","taskschd.iidlesettings_idleduration","taskschd/IIdleSettings::IdleDuration","taskschd/IIdleSettings::get_IdleDuration","taskschd/IIdleSettings::put_IdleDuration"]
old-location: taskschd\iidlesettings_idleduration.htm
tech.root: taskschd
ms.assetid: c50a0fb5-053f-4941-ab10-67efefdcbe59
ms.date: 12/05/2018
ms.keywords: IIdleSettings interface [Task Scheduler],IdleDuration property, IIdleSettings.IdleDuration, IIdleSettings.put_IdleDuration, IIdleSettings::IdleDuration, IIdleSettings::get_IdleDuration, IIdleSettings::put_IdleDuration, IdleDuration property [Task Scheduler], IdleDuration property [Task Scheduler],IIdleSettings interface, put_IdleDuration, taskschd.iidlesettings_idleduration, taskschd/IIdleSettings::IdleDuration, taskschd/IIdleSettings::get_IdleDuration, taskschd/IIdleSettings::put_IdleDuration
f1_keywords:
- taskschd/IIdleSettings.IdleDuration
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
- IIdleSettings.IdleDuration
- IIdleSettings.get_IdleDuration
- IIdleSettings.put_IdleDuration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdleSettings::put_IdleDuration


## -description


 Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-duration-idlesettingstype-element">Duration</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

