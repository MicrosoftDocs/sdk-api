---
UID: NN:taskschd.ITaskSettings2
title: ITaskSettings2
author: windows-sdk-content
description: Provides the extended settings that the Task Scheduler uses to run the task.
old-location: taskschd\itasksettings2.htm
old-project: taskschd
ms.assetid: ea08e599-5d4a-4919-abed-c35fe0977f3f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskSettings2, ITaskSettings2 interface [Task Scheduler], ITaskSettings2 interface [Task Scheduler],described, taskschd.itasksettings2, taskschd/ITaskSettings2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
 - ITaskSettings2
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings2 interface


## -description


 Provides the extended settings that the Task Scheduler uses to run the task.


## -remarks



When reading or writing XML for a task, the task settings are defined in the  <a href="https://msdn.microsoft.com/72d2929a-0dd2-44cd-be7b-72eca23a5e14">Settings</a> element of the Task Scheduler schema.


#### Examples

For more information and a code example for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.   

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a>



<a href="https://msdn.microsoft.com/831e1259-df2b-4b03-8336-706727fd7b14">INetworkSettings</a>



<a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a>
 

 

