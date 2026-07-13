---
UID: NF:taskschd.IRegistrationInfo.put_Source
title: IRegistrationInfo::put_Source (taskschd.h)
description: Gets or sets where the task originated from. For example, a task may originate from a component, service, application, or user. (Put)
helpviewer_keywords: ["IRegistrationInfo interface [Task Scheduler]","Source property","IRegistrationInfo.Source","IRegistrationInfo.put_Source","IRegistrationInfo::Source","IRegistrationInfo::get_Source","IRegistrationInfo::put_Source","Source property [Task Scheduler]","Source property [Task Scheduler]","IRegistrationInfo interface","put_Source","taskschd.iregistrationinfo_source","taskschd/IRegistrationInfo::Source","taskschd/IRegistrationInfo::get_Source","taskschd/IRegistrationInfo::put_Source"]
old-location: taskschd\iregistrationinfo_source.htm
tech.root: taskschd
ms.assetid: 538d48f9-671d-452b-8e78-86954342a28f
ms.date: 12/05/2018
ms.keywords: IRegistrationInfo interface [Task Scheduler],Source property, IRegistrationInfo.Source, IRegistrationInfo.put_Source, IRegistrationInfo::Source, IRegistrationInfo::get_Source, IRegistrationInfo::put_Source, Source property [Task Scheduler], Source property [Task Scheduler],IRegistrationInfo interface, put_Source, taskschd.iregistrationinfo_source, taskschd/IRegistrationInfo::Source, taskschd/IRegistrationInfo::get_Source, taskschd/IRegistrationInfo::put_Source
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
 - IRegistrationInfo::put_Source
 - taskschd/IRegistrationInfo::put_Source
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
 - IRegistrationInfo.Source
 - IRegistrationInfo.get_Source
 - IRegistrationInfo.put_Source
---

# IRegistrationInfo::put_Source


## -description

Gets or sets where the task originated from. For example, a task may originate from a component, service, application, or user.

This property is read/write.

## -parameters

## -remarks

The Task Scheduler UI uses the source to sort tasks. For example, tasks could be sorted by component, service, application, or user.

When reading or writing XML for a task, the task source information is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-source-registrationinfotype-element">Source</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
