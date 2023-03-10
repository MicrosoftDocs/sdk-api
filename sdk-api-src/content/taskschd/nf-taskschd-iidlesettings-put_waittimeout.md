---
UID: NF:taskschd.IIdleSettings.put_WaitTimeout
title: IIdleSettings::put_WaitTimeout (taskschd.h)
description: Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur. (Put)
helpviewer_keywords: ["IIdleSettings interface [Task Scheduler]","WaitTimeout property","IIdleSettings.WaitTimeout","IIdleSettings.put_WaitTimeout","IIdleSettings::WaitTimeout","IIdleSettings::get_WaitTimeout","IIdleSettings::put_WaitTimeout","WaitTimeout property [Task Scheduler]","WaitTimeout property [Task Scheduler]","IIdleSettings interface","put_WaitTimeout","taskschd.iidlesettings_waittimeout","taskschd/IIdleSettings::WaitTimeout","taskschd/IIdleSettings::get_WaitTimeout","taskschd/IIdleSettings::put_WaitTimeout"]
old-location: taskschd\iidlesettings_waittimeout.htm
tech.root: taskschd
ms.assetid: fff7f954-4e57-42bf-ad86-5ddede94279c
ms.date: 12/05/2018
ms.keywords: IIdleSettings interface [Task Scheduler],WaitTimeout property, IIdleSettings.WaitTimeout, IIdleSettings.put_WaitTimeout, IIdleSettings::WaitTimeout, IIdleSettings::get_WaitTimeout, IIdleSettings::put_WaitTimeout, WaitTimeout property [Task Scheduler], WaitTimeout property [Task Scheduler],IIdleSettings interface, put_WaitTimeout, taskschd.iidlesettings_waittimeout, taskschd/IIdleSettings::WaitTimeout, taskschd/IIdleSettings::get_WaitTimeout, taskschd/IIdleSettings::put_WaitTimeout
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
 - IIdleSettings::put_WaitTimeout
 - taskschd/IIdleSettings::put_WaitTimeout
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
 - IIdleSettings.WaitTimeout
 - IIdleSettings.get_WaitTimeout
 - IIdleSettings.put_WaitTimeout
---

# IIdleSettings::put_WaitTimeout


## -description

Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur. If no value  is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-waittimeout-idlesettingstype-element">WaitTimeout</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <b>WaitTimeout</b> property of the <a href="/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a> interface is ignored.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
