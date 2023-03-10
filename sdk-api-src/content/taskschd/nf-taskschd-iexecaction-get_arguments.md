---
UID: NF:taskschd.IExecAction.get_Arguments
title: IExecAction::get_Arguments (taskschd.h)
description: Gets or sets the arguments associated with the command-line operation. (Get)
helpviewer_keywords: ["Arguments property [Task Scheduler]","Arguments property [Task Scheduler]","IExecAction interface","IExecAction interface [Task Scheduler]","Arguments property","IExecAction.Arguments","IExecAction.get_Arguments","IExecAction::Arguments","IExecAction::get_Arguments","IExecAction::put_Arguments","get_Arguments","taskschd.iexecaction_arguments","taskschd/IExecAction::Arguments","taskschd/IExecAction::get_Arguments","taskschd/IExecAction::put_Arguments"]
old-location: taskschd\iexecaction_arguments.htm
tech.root: taskschd
ms.assetid: 623b3ffb-ff0f-46bf-ae3d-146e38c8bbc8
ms.date: 12/05/2018
ms.keywords: Arguments property [Task Scheduler], Arguments property [Task Scheduler],IExecAction interface, IExecAction interface [Task Scheduler],Arguments property, IExecAction.Arguments, IExecAction.get_Arguments, IExecAction::Arguments, IExecAction::get_Arguments, IExecAction::put_Arguments, get_Arguments, taskschd.iexecaction_arguments, taskschd/IExecAction::Arguments, taskschd/IExecAction::get_Arguments, taskschd/IExecAction::put_Arguments
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
 - IExecAction::get_Arguments
 - taskschd/IExecAction::get_Arguments
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
 - IExecAction.Arguments
 - IExecAction.get_Arguments
 - IExecAction.put_Arguments
---

# IExecAction::get_Arguments


## -description

Gets or sets the arguments associated with the command-line operation.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML, the command-line operation arguments are specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-arguments-exectype-element">Arguments</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iexecaction">IExecAction</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
