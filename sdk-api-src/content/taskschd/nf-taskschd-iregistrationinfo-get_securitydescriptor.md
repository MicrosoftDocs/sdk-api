---
UID: NF:taskschd.IRegistrationInfo.get_SecurityDescriptor
title: IRegistrationInfo::get_SecurityDescriptor (taskschd.h)
description: Gets or sets the security descriptor of the task. (Get)
helpviewer_keywords: ["IRegistrationInfo interface [Task Scheduler]","SecurityDescriptor property","IRegistrationInfo.SecurityDescriptor","IRegistrationInfo.get_SecurityDescriptor","IRegistrationInfo::SecurityDescriptor","IRegistrationInfo::get_SecurityDescriptor","IRegistrationInfo::put_SecurityDescriptor","SecurityDescriptor property [Task Scheduler]","SecurityDescriptor property [Task Scheduler]","IRegistrationInfo interface","get_SecurityDescriptor","taskschd.iregistrationinfo_securitydescriptor","taskschd/IRegistrationInfo::SecurityDescriptor","taskschd/IRegistrationInfo::get_SecurityDescriptor","taskschd/IRegistrationInfo::put_SecurityDescriptor"]
old-location: taskschd\iregistrationinfo_securitydescriptor.htm
tech.root: taskschd
ms.assetid: 095b8f81-412a-461d-bb6e-65c10b337d3e
ms.date: 12/05/2018
ms.keywords: IRegistrationInfo interface [Task Scheduler],SecurityDescriptor property, IRegistrationInfo.SecurityDescriptor, IRegistrationInfo.get_SecurityDescriptor, IRegistrationInfo::SecurityDescriptor, IRegistrationInfo::get_SecurityDescriptor, IRegistrationInfo::put_SecurityDescriptor, SecurityDescriptor property [Task Scheduler], SecurityDescriptor property [Task Scheduler],IRegistrationInfo interface, get_SecurityDescriptor, taskschd.iregistrationinfo_securitydescriptor, taskschd/IRegistrationInfo::SecurityDescriptor, taskschd/IRegistrationInfo::get_SecurityDescriptor, taskschd/IRegistrationInfo::put_SecurityDescriptor
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
 - IRegistrationInfo::get_SecurityDescriptor
 - taskschd/IRegistrationInfo::get_SecurityDescriptor
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
 - IRegistrationInfo.SecurityDescriptor
 - IRegistrationInfo.get_SecurityDescriptor
 - IRegistrationInfo.put_SecurityDescriptor
---

# IRegistrationInfo::get_SecurityDescriptor


## -description

Gets or sets the security descriptor of the task. If a different security descriptor is supplied during task registration, it will supersede the security descriptor that is set with this property.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the security descriptor of the task is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-securitydescriptor-registrationinfotype-element">SecurityDescriptor</a> element of the Task Scheduler schema.

If a different security descriptor is supplied when a task is  registered, then it will supersede the <i>sddl</i> parameter that is set through this property.

If you try to pass an invalid security descriptor into the <i>sddl</i> parameter, then this method will return <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
