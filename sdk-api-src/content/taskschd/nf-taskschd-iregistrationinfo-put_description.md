---
UID: NF:taskschd.IRegistrationInfo.put_Description
title: IRegistrationInfo::put_Description (taskschd.h)
description: Gets or sets the description of the task.
helpviewer_keywords: ["Description property [Task Scheduler]","Description property [Task Scheduler]","IRegistrationInfo interface","IRegistrationInfo interface [Task Scheduler]","Description property","IRegistrationInfo.Description","IRegistrationInfo.put_Description","IRegistrationInfo::Description","IRegistrationInfo::get_Description","IRegistrationInfo::put_Description","put_Description","taskschd.iregistrationinfo_description","taskschd/IRegistrationInfo::Description","taskschd/IRegistrationInfo::get_Description","taskschd/IRegistrationInfo::put_Description"]
old-location: taskschd\iregistrationinfo_description.htm
tech.root: taskschd
ms.assetid: 03b0f62c-0f2b-4e0a-8518-de3b94f6a197
ms.date: 12/05/2018
ms.keywords: Description property [Task Scheduler], Description property [Task Scheduler],IRegistrationInfo interface, IRegistrationInfo interface [Task Scheduler],Description property, IRegistrationInfo.Description, IRegistrationInfo.put_Description, IRegistrationInfo::Description, IRegistrationInfo::get_Description, IRegistrationInfo::put_Description, put_Description, taskschd.iregistrationinfo_description, taskschd/IRegistrationInfo::Description, taskschd/IRegistrationInfo::get_Description, taskschd/IRegistrationInfo::put_Description
f1_keywords:
- taskschd/IRegistrationInfo.Description
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- IRegistrationInfo.Description
- IRegistrationInfo.get_Description
- IRegistrationInfo.put_Description
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegistrationInfo::put_Description


## -description


Gets or sets the description of the task.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the description of the task is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-description-registrationinfotype-element">Description</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

