---
UID: NF:taskschd.ITaskSettings.put_AllowHardTerminate
title: ITaskSettings::put_AllowHardTerminate (taskschd.h)
description: Gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using TerminateProcess. (Put)
helpviewer_keywords: ["AllowHardTerminate property [Task Scheduler]","AllowHardTerminate property [Task Scheduler]","ITaskSettings interface","AllowHardTerminate property [Task Scheduler]","TaskSettings class","ITaskSettings interface [Task Scheduler]","AllowHardTerminate property","ITaskSettings.AllowHardTerminate","ITaskSettings.put_AllowHardTerminate","ITaskSettings::AllowHardTerminate","ITaskSettings::get_AllowHardTerminate","ITaskSettings::put_AllowHardTerminate","TaskSettings class [Task Scheduler]","AllowHardTerminate property","put_AllowHardTerminate","taskschd.itasksettings_allowhardterminate","taskschd/ITaskSettings::AllowHardTerminate","taskschd/ITaskSettings::get_AllowHardTerminate","taskschd/ITaskSettings::put_AllowHardTerminate"]
old-location: taskschd\itasksettings_allowhardterminate.htm
tech.root: taskschd
ms.assetid: fd8105cf-5ef1-4ae4-8bb7-05469758b6b4
ms.date: 12/05/2018
ms.keywords: AllowHardTerminate property [Task Scheduler], AllowHardTerminate property [Task Scheduler],ITaskSettings interface, AllowHardTerminate property [Task Scheduler],TaskSettings class, ITaskSettings interface [Task Scheduler],AllowHardTerminate property, ITaskSettings.AllowHardTerminate, ITaskSettings.put_AllowHardTerminate, ITaskSettings::AllowHardTerminate, ITaskSettings::get_AllowHardTerminate, ITaskSettings::put_AllowHardTerminate, TaskSettings class [Task Scheduler],AllowHardTerminate property, put_AllowHardTerminate, taskschd.itasksettings_allowhardterminate, taskschd/ITaskSettings::AllowHardTerminate, taskschd/ITaskSettings::get_AllowHardTerminate, taskschd/ITaskSettings::put_AllowHardTerminate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskSettings::put_AllowHardTerminate
 - taskschd/ITaskSettings::put_AllowHardTerminate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.AllowHardTerminate
 - ITaskSettings.get_AllowHardTerminate
 - ITaskSettings.put_AllowHardTerminate
 - TaskSettings.AllowHardTerminate
---

# ITaskSettings::put_AllowHardTerminate


## -description

Gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using  <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>. The service will try to close the running task by sending the <a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a> notification, and if the  task does not respond, the task will be terminated only if this property is set to true.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-allowhardterminate-settingstype-element">AllowHardTerminate</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



TaskSettings
