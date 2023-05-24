---
UID: NN:taskschd.ITaskSettings2
title: ITaskSettings2 (taskschd.h)
description: Provides the extended settings that the Task Scheduler uses to run the task. (ITaskSettings2)
helpviewer_keywords: ["ITaskSettings2","ITaskSettings2 interface [Task Scheduler]","ITaskSettings2 interface [Task Scheduler]","described","taskschd.itasksettings2","taskschd/ITaskSettings2"]
old-location: taskschd\itasksettings2.htm
tech.root: taskschd
ms.assetid: ea08e599-5d4a-4919-abed-c35fe0977f3f
ms.date: 12/05/2018
ms.keywords: ITaskSettings2, ITaskSettings2 interface [Task Scheduler], ITaskSettings2 interface [Task Scheduler],described, taskschd.itasksettings2, taskschd/ITaskSettings2
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
 - ITaskSettings2
 - taskschd/ITaskSettings2
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
 - ITaskSettings2
---

# ITaskSettings2 interface


## -description

 Provides the extended settings that the Task Scheduler uses to run the task.

## -remarks

When reading or writing XML for a task, the task settings are defined in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-settings-tasktype-element">Settings</a> element of the Task Scheduler schema.


#### Examples

For more information and a code example for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.   

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-inetworksettings">INetworkSettings</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a>
