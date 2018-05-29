---
UID: NF:taskschd.IPrincipal.get_DisplayName
title: IPrincipal::get_DisplayName
author: windows-sdk-content
description: Gets or sets the name of the principal.
old-location: taskschd\iprincipal_displayname.htm
old-project: TaskSchd
ms.assetid: 285a0e64-d796-4b0d-84b1-9ebd0728ddc0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: DisplayName property [Task Scheduler], DisplayName property [Task Scheduler],IPrincipal interface, IPrincipal interface [Task Scheduler],DisplayName property, IPrincipal.DisplayName, IPrincipal.get_DisplayName, IPrincipal::DisplayName, IPrincipal::get_DisplayName, IPrincipal::put_DisplayName, get_DisplayName, taskschd.iprincipal_displayname, taskschd/IPrincipal::DisplayName, taskschd/IPrincipal::get_DisplayName, taskschd/IPrincipal::put_DisplayName
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IPrincipal.DisplayName
-	IPrincipal.get_DisplayName
-	IPrincipal.put_DisplayName
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IPrincipal::get_DisplayName


## -description


Gets or sets the name of the principal.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the display name for a principal is specified in the <a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

