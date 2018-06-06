---
UID: NF:taskschd.IIdleSettings.put_WaitTimeout
title: IIdleSettings::put_WaitTimeout
author: windows-sdk-content
description: Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.
old-location: taskschd\iidlesettings_waittimeout.htm
old-project: TaskSchd
ms.assetid: fff7f954-4e57-42bf-ad86-5ddede94279c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IIdleSettings interface [Task Scheduler],WaitTimeout property, IIdleSettings.WaitTimeout, IIdleSettings.put_WaitTimeout, IIdleSettings::WaitTimeout, IIdleSettings::get_WaitTimeout, IIdleSettings::put_WaitTimeout, WaitTimeout property [Task Scheduler], WaitTimeout property [Task Scheduler],IIdleSettings interface, put_WaitTimeout, taskschd.iidlesettings_waittimeout, taskschd/IIdleSettings::WaitTimeout, taskschd/IIdleSettings::get_WaitTimeout, taskschd/IIdleSettings::put_WaitTimeout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
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
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IIdleSettings::put_WaitTimeout


## -description


Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur. If no value  is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/6a4cc80d-adc2-47a7-946f-a9f12eeb35a4">WaitTimeout</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <b>WaitTimeout</b> property of the <a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a> interface is ignored.




## -see-also




<a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

