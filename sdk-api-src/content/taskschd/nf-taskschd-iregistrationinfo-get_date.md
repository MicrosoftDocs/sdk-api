---
UID: NF:taskschd.IRegistrationInfo.get_Date
title: IRegistrationInfo::get_Date (taskschd.h)
description: Gets or sets the date and time when the task is registered. (Get)
helpviewer_keywords: ["Date property [Task Scheduler]","Date property [Task Scheduler]","IRegistrationInfo interface","IRegistrationInfo interface [Task Scheduler]","Date property","IRegistrationInfo.Date","IRegistrationInfo.get_Date","IRegistrationInfo::Date","IRegistrationInfo::get_Date","IRegistrationInfo::put_Date","get_Date","taskschd.iregistrationinfo_date","taskschd/IRegistrationInfo::Date","taskschd/IRegistrationInfo::get_Date","taskschd/IRegistrationInfo::put_Date"]
old-location: taskschd\iregistrationinfo_date.htm
tech.root: taskschd
ms.assetid: b9a41413-954f-447c-8fce-f99c81fec40a
ms.date: 12/05/2018
ms.keywords: Date property [Task Scheduler], Date property [Task Scheduler],IRegistrationInfo interface, IRegistrationInfo interface [Task Scheduler],Date property, IRegistrationInfo.Date, IRegistrationInfo.get_Date, IRegistrationInfo::Date, IRegistrationInfo::get_Date, IRegistrationInfo::put_Date, get_Date, taskschd.iregistrationinfo_date, taskschd/IRegistrationInfo::Date, taskschd/IRegistrationInfo::get_Date, taskschd/IRegistrationInfo::put_Date
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
 - IRegistrationInfo::get_Date
 - taskschd/IRegistrationInfo::get_Date
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
 - IRegistrationInfo.Date
 - IRegistrationInfo.get_Date
 - IRegistrationInfo.put_Date
---

# IRegistrationInfo::get_Date


## -description

Gets or sets the date and time when the task is registered.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the registration date is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-date-registrationinfotype-element">Date</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
