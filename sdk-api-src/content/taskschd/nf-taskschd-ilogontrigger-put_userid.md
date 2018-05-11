---
UID: NF:taskschd.ILogonTrigger.put_UserId
title: ILogonTrigger::put_UserId
author: windows-driver-content
description: Gets or sets the identifier of the user.
old-location: taskschd\ilogontrigger_userid.htm
old-project: TaskSchd
ms.assetid: 22d69609-1400-41eb-ae25-4ca05c4733ba
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ILogonTrigger interface [Task Scheduler],UserId property, ILogonTrigger.UserId, ILogonTrigger.put_UserId, ILogonTrigger::UserId, ILogonTrigger::get_UserId, ILogonTrigger::put_UserId, UserId property [Task Scheduler], UserId property [Task Scheduler],ILogonTrigger interface, put_UserId, taskschd.ilogontrigger_userid, taskschd/ILogonTrigger::UserId, taskschd/ILogonTrigger::get_UserId, taskschd/ILogonTrigger::put_UserId
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
-	ILogonTrigger.UserId
-	ILogonTrigger.get_UserId
-	ILogonTrigger.put_UserId
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILogonTrigger::put_UserId


## -description


Gets or sets the identifier of the user.

This property is read/write.


## -parameters


## -remarks



If you want a task to be triggered when any member of a group logs on to the computer rather than when  a specific user logs on, then do not assign a value to the  <b>UserId</b> property.  Instead, create a logon trigger with an empty <b>UserId</b> property and assign a value to the principal for the task using the <a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId</a> property.

When reading or writing XML for a task, the logon user identifier is specified using the <a href="https://msdn.microsoft.com/52568899-e351-4ee1-b613-d7c42d7b983d">UserId</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/c0206a18-53f2-4def-8f54-2b175a0579f4">ILogonTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

