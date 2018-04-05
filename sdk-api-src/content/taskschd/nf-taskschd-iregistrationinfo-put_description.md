---
UID: NF:taskschd.IRegistrationInfo.put_Description
title: IRegistrationInfo::put_Description method
author: windows-driver-content
description: Gets or sets the description of the task.
old-location: taskschd\iregistrationinfo_description.htm
old-project: TaskSchd
ms.assetid: 03b0f62c-0f2b-4e0a-8518-de3b94f6a197
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Description property [Task Scheduler], Description property [Task Scheduler], IRegistrationInfo interface, IRegistrationInfo, IRegistrationInfo interface [Task Scheduler], Description property, IRegistrationInfo.Description, IRegistrationInfo::get_Description, IRegistrationInfo::put_Description, put_Description,IRegistrationInfo.put_Description, taskschd.iregistrationinfo_description, taskschd/IRegistrationInfo::Description, taskschd/IRegistrationInfo::get_Description, taskschd/IRegistrationInfo::put_Description
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
-	IRegistrationInfo.Description
-	IRegistrationInfo.get_Description
-	IRegistrationInfo.put_Description
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegistrationInfo::put_Description method


## -description


Gets or sets the description of the task.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the description of the task is specified using the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/e04f0c47-ab89-49e4-aac6-028d2555ecf1">IRegistrationInfo</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

