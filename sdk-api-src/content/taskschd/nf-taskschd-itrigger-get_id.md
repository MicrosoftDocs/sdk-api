---
UID: NF:taskschd.ITrigger.get_Id
title: ITrigger::get_Id
author: windows-sdk-content
description: Gets or sets the identifier for the trigger.
old-location: taskschd\itrigger_id.htm
old-project: TaskSchd
ms.assetid: 7cf26e63-2517-44a0-9a12-06c2a903c089
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITrigger interface [Task Scheduler],Id property, ITrigger.Id, ITrigger.get_Id, ITrigger::Id, ITrigger::get_Id, ITrigger::put_Id, Id property [Task Scheduler], Id property [Task Scheduler],ITrigger interface, get_Id, taskschd.itrigger_id, taskschd/ITrigger::Id, taskschd/ITrigger::get_Id, taskschd/ITrigger::put_Id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.redist: 
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
 - ITrigger.Id
 - ITrigger.get_Id
 - ITrigger.put_Id
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITrigger::get_Id


## -description


Gets or sets the identifier for the trigger.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the  <a href="https://msdn.microsoft.com/c6833547-0daf-4e8a-b8c5-b422827b1d96">BootTrigger</a> element) of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

