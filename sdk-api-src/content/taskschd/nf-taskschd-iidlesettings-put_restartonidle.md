---
UID: NF:taskschd.IIdleSettings.put_RestartOnIdle
title: IIdleSettings::put_RestartOnIdle (taskschd.h)
description: Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once. (Put)
helpviewer_keywords: ["IIdleSettings interface [Task Scheduler]","RestartOnIdle property","IIdleSettings.RestartOnIdle","IIdleSettings.put_RestartOnIdle","IIdleSettings::RestartOnIdle","IIdleSettings::get_RestartOnIdle","IIdleSettings::put_RestartOnIdle","RestartOnIdle property [Task Scheduler]","RestartOnIdle property [Task Scheduler]","IIdleSettings interface","put_RestartOnIdle","taskschd.iidlesettings_restartonidle","taskschd/IIdleSettings::RestartOnIdle","taskschd/IIdleSettings::get_RestartOnIdle","taskschd/IIdleSettings::put_RestartOnIdle"]
old-location: taskschd\iidlesettings_restartonidle.htm
tech.root: taskschd
ms.assetid: 42779c7d-4739-47c5-bf35-5d6c612c59c0
ms.date: 12/05/2018
ms.keywords: IIdleSettings interface [Task Scheduler],RestartOnIdle property, IIdleSettings.RestartOnIdle, IIdleSettings.put_RestartOnIdle, IIdleSettings::RestartOnIdle, IIdleSettings::get_RestartOnIdle, IIdleSettings::put_RestartOnIdle, RestartOnIdle property [Task Scheduler], RestartOnIdle property [Task Scheduler],IIdleSettings interface, put_RestartOnIdle, taskschd.iidlesettings_restartonidle, taskschd/IIdleSettings::RestartOnIdle, taskschd/IIdleSettings::get_RestartOnIdle, taskschd/IIdleSettings::put_RestartOnIdle
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
 - IIdleSettings::put_RestartOnIdle
 - taskschd/IIdleSettings::put_RestartOnIdle
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
 - IIdleSettings.RestartOnIdle
 - IIdleSettings.get_RestartOnIdle
 - IIdleSettings.put_RestartOnIdle
---

# IIdleSettings::put_RestartOnIdle


## -description

Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.

This property is read/write.

## -parameters

## -remarks

This property is only used if the <a href="/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend">StopOnIdleEnd</a> property is set to True.

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-restartonidle-idlesettingstype-element">RestartOnIdle</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
