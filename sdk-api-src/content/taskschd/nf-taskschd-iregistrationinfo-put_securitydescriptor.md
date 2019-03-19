---
UID: NF:taskschd.IRegistrationInfo.put_SecurityDescriptor
title: IRegistrationInfo::put_SecurityDescriptor (taskschd.h)
author: windows-sdk-content
description: Gets or sets the security descriptor of the task.
old-location: taskschd\iregistrationinfo_securitydescriptor.htm
tech.root: taskschd
ms.assetid: 095b8f81-412a-461d-bb6e-65c10b337d3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRegistrationInfo interface [Task Scheduler],SecurityDescriptor property, IRegistrationInfo.SecurityDescriptor, IRegistrationInfo.put_SecurityDescriptor, IRegistrationInfo::SecurityDescriptor, IRegistrationInfo::get_SecurityDescriptor, IRegistrationInfo::put_SecurityDescriptor, SecurityDescriptor property [Task Scheduler], SecurityDescriptor property [Task Scheduler],IRegistrationInfo interface, put_SecurityDescriptor, taskschd.iregistrationinfo_securitydescriptor, taskschd/IRegistrationInfo::SecurityDescriptor, taskschd/IRegistrationInfo::get_SecurityDescriptor, taskschd/IRegistrationInfo::put_SecurityDescriptor
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
 - IRegistrationInfo.SecurityDescriptor
 - IRegistrationInfo.get_SecurityDescriptor
 - IRegistrationInfo.put_SecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegistrationInfo::put_SecurityDescriptor


## -description


Gets or sets the security descriptor of the task. If a different security descriptor is supplied during task registration, it will supersede the security descriptor that is set with this property.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the security descriptor of the task is specified using the <a href="https://msdn.microsoft.com/79821b20-226a-4e7e-8ca1-6c9cf9f1b56e">SecurityDescriptor</a> element of the Task Scheduler schema.

If a different security descriptor is supplied when a task is  registered, then it will supersede the <i>sddl</i> parameter that is set through this property.

If you try to pass an invalid security descriptor into the <i>sddl</i> parameter, then this method will return <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/e04f0c47-ab89-49e4-aac6-028d2555ecf1">IRegistrationInfo</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

