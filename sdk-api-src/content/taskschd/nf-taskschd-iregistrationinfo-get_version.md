---
UID: NF:taskschd.IRegistrationInfo.get_Version
title: IRegistrationInfo::get_Version (taskschd.h)
description: Gets or sets the version number of the task. (Get)
helpviewer_keywords: ["IRegistrationInfo interface [Task Scheduler]","Version property","IRegistrationInfo.Version","IRegistrationInfo.get_Version","IRegistrationInfo::Version","IRegistrationInfo::get_Version","IRegistrationInfo::put_Version","Version property [Task Scheduler]","Version property [Task Scheduler]","IRegistrationInfo interface","get_Version","taskschd.iregistrationinfo_version","taskschd/IRegistrationInfo::Version","taskschd/IRegistrationInfo::get_Version","taskschd/IRegistrationInfo::put_Version"]
old-location: taskschd\iregistrationinfo_version.htm
tech.root: taskschd
ms.assetid: e2305dbd-bb81-4854-86bd-d0c4f3cf78a1
ms.date: 12/05/2018
ms.keywords: IRegistrationInfo interface [Task Scheduler],Version property, IRegistrationInfo.Version, IRegistrationInfo.get_Version, IRegistrationInfo::Version, IRegistrationInfo::get_Version, IRegistrationInfo::put_Version, Version property [Task Scheduler], Version property [Task Scheduler],IRegistrationInfo interface, get_Version, taskschd.iregistrationinfo_version, taskschd/IRegistrationInfo::Version, taskschd/IRegistrationInfo::get_Version, taskschd/IRegistrationInfo::put_Version
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
 - IRegistrationInfo::get_Version
 - taskschd/IRegistrationInfo::get_Version
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
 - IRegistrationInfo.Version
 - IRegistrationInfo.get_Version
 - IRegistrationInfo.put_Version
---

# IRegistrationInfo::get_Version


## -description

Gets or sets the version number of the task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the version number of the task is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-version-registrationinfotype-element">Version</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
