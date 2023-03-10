---
UID: NF:taskschd.IRegistrationInfo.get_Documentation
title: IRegistrationInfo::get_Documentation (taskschd.h)
description: Gets or sets any additional documentation for the task. (Get)
helpviewer_keywords: ["Documentation property [Task Scheduler]","Documentation property [Task Scheduler]","IRegistrationInfo interface","IRegistrationInfo interface [Task Scheduler]","Documentation property","IRegistrationInfo.Documentation","IRegistrationInfo.get_Documentation","IRegistrationInfo::Documentation","IRegistrationInfo::get_Documentation","IRegistrationInfo::put_Documentation","get_Documentation","taskschd.iregistrationinfo_documentation","taskschd/IRegistrationInfo::Documentation","taskschd/IRegistrationInfo::get_Documentation","taskschd/IRegistrationInfo::put_Documentation"]
old-location: taskschd\iregistrationinfo_documentation.htm
tech.root: taskschd
ms.assetid: ec12b0aa-def4-4ff3-b067-62f989c890d5
ms.date: 12/05/2018
ms.keywords: Documentation property [Task Scheduler], Documentation property [Task Scheduler],IRegistrationInfo interface, IRegistrationInfo interface [Task Scheduler],Documentation property, IRegistrationInfo.Documentation, IRegistrationInfo.get_Documentation, IRegistrationInfo::Documentation, IRegistrationInfo::get_Documentation, IRegistrationInfo::put_Documentation, get_Documentation, taskschd.iregistrationinfo_documentation, taskschd/IRegistrationInfo::Documentation, taskschd/IRegistrationInfo::get_Documentation, taskschd/IRegistrationInfo::put_Documentation
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
 - IRegistrationInfo::get_Documentation
 - taskschd/IRegistrationInfo::get_Documentation
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
 - IRegistrationInfo.Documentation
 - IRegistrationInfo.get_Documentation
 - IRegistrationInfo.put_Documentation
---

# IRegistrationInfo::get_Documentation


## -description

Gets or sets any additional documentation for the task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the additional documentation for the task is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-documentation-registrationinfotype-element">Documentation</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
