---
UID: NF:taskschd.IRegistrationInfo.put_Source
title: IRegistrationInfo::put_Source method
author: windows-driver-content
description: Gets or sets where the task originated from. For example, a task may originate from a component, service, application, or user.
old-location: taskschd\iregistrationinfo_source.htm
old-project: TaskSchd
ms.assetid: 538d48f9-671d-452b-8e78-86954342a28f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRegistrationInfo, IRegistrationInfo interface [Task Scheduler], Source property, IRegistrationInfo.Source, IRegistrationInfo::get_Source, IRegistrationInfo::put_Source, Source property [Task Scheduler], Source property [Task Scheduler], IRegistrationInfo interface, put_Source,IRegistrationInfo.put_Source, taskschd.iregistrationinfo_source, taskschd/IRegistrationInfo::Source, taskschd/IRegistrationInfo::get_Source, taskschd/IRegistrationInfo::put_Source
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IRegistrationInfo.Source
-	IRegistrationInfo.get_Source
-	IRegistrationInfo.put_Source
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegistrationInfo::put_Source method


## -description


Gets or sets where the task originated from. For example, a task may originate from a component, service, application, or user.

This property is read/write.


## -parameters


## -remarks



The Task Scheduler UI uses the source to sort tasks. For example, tasks could be sorted by component, service, application, or user.

When reading or writing XML for a task, the task source information is specified using the <a href="https://msdn.microsoft.com/174e2aac-7cd0-4c19-9441-2c93a3260c6f">Source</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/e04f0c47-ab89-49e4-aac6-028d2555ecf1">IRegistrationInfo</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

