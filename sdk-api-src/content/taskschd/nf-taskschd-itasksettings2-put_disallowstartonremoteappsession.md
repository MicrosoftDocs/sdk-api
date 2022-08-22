---
UID: NF:taskschd.ITaskSettings2.put_DisallowStartOnRemoteAppSession
title: ITaskSettings2::put_DisallowStartOnRemoteAppSession (taskschd.h)
description: Gets or sets a Boolean value that specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session. (Put)
helpviewer_keywords: ["DisallowStartOnRemoteAppSession property [Task Scheduler]","DisallowStartOnRemoteAppSession property [Task Scheduler]","ITaskSettings2 interface","ITaskSettings2 interface [Task Scheduler]","DisallowStartOnRemoteAppSession property","ITaskSettings2.DisallowStartOnRemoteAppSession","ITaskSettings2.put_DisallowStartOnRemoteAppSession","ITaskSettings2::DisallowStartOnRemoteAppSession","ITaskSettings2::get_DisallowStartOnRemoteAppSession","ITaskSettings2::put_DisallowStartOnRemoteAppSession","put_DisallowStartOnRemoteAppSession","taskschd.itasksettings2_disallowstartonremoteappsession","taskschd/ITaskSettings2::DisallowStartOnRemoteAppSession","taskschd/ITaskSettings2::get_DisallowStartOnRemoteAppSession","taskschd/ITaskSettings2::put_DisallowStartOnRemoteAppSession"]
old-location: taskschd\itasksettings2_disallowstartonremoteappsession.htm
tech.root: taskschd
ms.assetid: a951d824-89a9-4483-a912-5c4cbf1755e1
ms.date: 12/05/2018
ms.keywords: DisallowStartOnRemoteAppSession property [Task Scheduler], DisallowStartOnRemoteAppSession property [Task Scheduler],ITaskSettings2 interface, ITaskSettings2 interface [Task Scheduler],DisallowStartOnRemoteAppSession property, ITaskSettings2.DisallowStartOnRemoteAppSession, ITaskSettings2.put_DisallowStartOnRemoteAppSession, ITaskSettings2::DisallowStartOnRemoteAppSession, ITaskSettings2::get_DisallowStartOnRemoteAppSession, ITaskSettings2::put_DisallowStartOnRemoteAppSession, put_DisallowStartOnRemoteAppSession, taskschd.itasksettings2_disallowstartonremoteappsession, taskschd/ITaskSettings2::DisallowStartOnRemoteAppSession, taskschd/ITaskSettings2::get_DisallowStartOnRemoteAppSession, taskschd/ITaskSettings2::put_DisallowStartOnRemoteAppSession
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
 - ITaskSettings2::put_DisallowStartOnRemoteAppSession
 - taskschd/ITaskSettings2::put_DisallowStartOnRemoteAppSession
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
 - ITaskSettings2.DisallowStartOnRemoteAppSession
 - ITaskSettings2.get_DisallowStartOnRemoteAppSession
 - ITaskSettings2.put_DisallowStartOnRemoteAppSession
---

# ITaskSettings2::put_DisallowStartOnRemoteAppSession


## -description

Gets or sets  a Boolean value that specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.

This property is read/write.

## -parameters

## -remarks

When reading or writing  XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-disallowstartonremoteappsession-settingstype-element">DisallowStartOnRemoteAppSession</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings2">ITaskSettings2</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
