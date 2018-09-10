---
UID: NN:taskschd.ILogonTrigger
title: ILogonTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task when a user logs on.
old-location: taskschd\ilogontrigger.htm
tech.root: TaskSchd
ms.assetid: c0206a18-53f2-4def-8f54-2b175a0579f4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ILogonTrigger, ILogonTrigger interface [Task Scheduler], ILogonTrigger interface [Task Scheduler],described, logon trigger [Task Scheduler],interface, taskschd.ilogontrigger, taskschd/ILogonTrigger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ILogonTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILogonTrigger interface


## -description


Represents a trigger that starts a task when a user logs on. When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.


## -remarks



If you want a task to be triggered when any member of a group logs on to the computer rather than when  a specific user logs on, then do not assign a value to the  <a href="https://msdn.microsoft.com/22d69609-1400-41eb-ae25-4ca05c4733ba">UserId</a> property.  Instead, create a logon trigger with an empty <b>UserId</b> property and assign a value to the principal for the task using the <a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId</a> property.

When reading or writing XML for a task, a logon trigger is specified using the <a href="https://msdn.microsoft.com/c3edee50-e053-4813-a1b2-bf1e7b575ff7">LogonTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/15647234-8d1f-4d75-b215-92927b300c1f">Logon Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

