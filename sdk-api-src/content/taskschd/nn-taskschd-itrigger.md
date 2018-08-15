---
UID: NN:taskschd.ITrigger
title: ITrigger
author: windows-sdk-content
description: Provides the common properties that are inherited by all trigger objects.
old-location: taskschd\itrigger.htm
old-project: taskschd
ms.assetid: 165297c1-704b-4ab3-a9e3-4aa3f10e07b1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITrigger, ITrigger interface [Task Scheduler], ITrigger interface [Task Scheduler],described, taskschd.itrigger, taskschd/ITrigger, triggers [Task Scheduler],trigger interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITrigger
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITrigger interface


## -description


Provides the common properties that are inherited by all trigger objects.


## -remarks




Task Scheduler provides the following individual interfaces for the different triggers that a task can use: 

<ul>
<li>
<a href="https://msdn.microsoft.com/8f186ee2-8d74-426c-9173-523a335422c9">IBootTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9980ddb1-9873-46d2-8dea-bfc3fd78bba8">IDailyTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aca5305f-68fc-4211-9f71-3f572340e94d">IIdleTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c0206a18-53f2-4def-8f54-2b175a0579f4">ILogonTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ed206a6-22e0-4131-92ce-29536ad65c6c">IMonthlyTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0862f7ac-69d6-4271-8d39-c5bd7038a95e">IRegistrationTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ebd5470-0801-42ff-a0c2-4d1e7f7ee365">ITimeTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c10b050a-8319-4e21-85aa-0bceb76abaaf">IWeeklyTrigger</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0bf56d67-6c44-4978-93a9-7b525f2bf140">ISessionStateChangeTrigger</a>
</li>
</ul>


When reading or writing XML, the triggers of a task are specified in the <a href="https://msdn.microsoft.com/4bf8e85e-3742-433d-821f-736fb2ff7139">Triggers</a> element of the Task Scheduler schema. 


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

