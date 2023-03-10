---
UID: NF:taskschd.IExecAction.put_Path
title: IExecAction::put_Path (taskschd.h)
description: Gets or sets the path to an executable file. (Put)
helpviewer_keywords: ["IExecAction interface [Task Scheduler]","Path property","IExecAction.Path","IExecAction.put_Path","IExecAction::Path","IExecAction::get_Path","IExecAction::put_Path","Path property [Task Scheduler]","Path property [Task Scheduler]","IExecAction interface","put_Path","taskschd.iexecaction_path","taskschd/IExecAction::Path","taskschd/IExecAction::get_Path","taskschd/IExecAction::put_Path"]
old-location: taskschd\iexecaction_path.htm
tech.root: taskschd
ms.assetid: 307e59e9-5460-40aa-bac7-fa8cb4755d35
ms.date: 12/05/2018
ms.keywords: IExecAction interface [Task Scheduler],Path property, IExecAction.Path, IExecAction.put_Path, IExecAction::Path, IExecAction::get_Path, IExecAction::put_Path, Path property [Task Scheduler], Path property [Task Scheduler],IExecAction interface, put_Path, taskschd.iexecaction_path, taskschd/IExecAction::Path, taskschd/IExecAction::get_Path, taskschd/IExecAction::put_Path
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
 - IExecAction::put_Path
 - taskschd/IExecAction::put_Path
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
 - IExecAction.Path
 - IExecAction.get_Path
 - IExecAction.put_Path
---

# IExecAction::put_Path


## -description

Gets or sets the path to an executable file.

This property is read/write.

## -parameters

## -remarks

This action performs a command-line operation. For example, the action could run a script or launch an executable.

When reading or writing XML, the command-line operation path is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-command-exectype-element">Command</a> element of the Task Scheduler schema.

The path is checked to make sure it is valid when the task is registered, not when this property is set.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iexecaction">IExecAction</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
