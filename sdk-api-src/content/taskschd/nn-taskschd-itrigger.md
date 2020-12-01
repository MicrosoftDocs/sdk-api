---
UID: NN:taskschd.ITrigger
title: ITrigger (taskschd.h)
description: Provides the common properties that are inherited by all trigger objects.
helpviewer_keywords: ["ITrigger","ITrigger interface [Task Scheduler]","ITrigger interface [Task Scheduler]","described","taskschd.itrigger","taskschd/ITrigger","triggers [Task Scheduler]","trigger interface"]
old-location: taskschd\itrigger.htm
tech.root: taskschd
ms.assetid: 165297c1-704b-4ab3-a9e3-4aa3f10e07b1
ms.date: 12/05/2018
ms.keywords: ITrigger, ITrigger interface [Task Scheduler], ITrigger interface [Task Scheduler],described, taskschd.itrigger, taskschd/ITrigger, triggers [Task Scheduler],trigger interface
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
 - ITrigger
 - taskschd/ITrigger
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
 - ITrigger
---

# ITrigger interface


## -description

Provides the common properties that are inherited by all trigger objects.

## -remarks

Task Scheduler provides the following individual interfaces for the different triggers that a task can use: 

<ul>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-iboottrigger">IBootTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-idailytrigger">IDailyTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-iidletrigger">IIdleTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger">ILogonTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger">IMonthlyDOWTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger">IMonthlyTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger">IRegistrationTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-itimetrigger">ITimeTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger">IWeeklyTrigger</a>
</li>
<li>
<a href="/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger">ISessionStateChangeTrigger</a>
</li>
</ul>


When reading or writing XML, the triggers of a task are specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-triggers-tasktype-element">Triggers</a> element of the Task Scheduler schema. 


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>