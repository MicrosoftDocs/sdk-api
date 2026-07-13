---
UID: NF:taskschd.IEventTrigger.put_Subscription
title: IEventTrigger::put_Subscription (taskschd.h)
description: Gets or sets a query string that identifies the event that fires the trigger. (Put)
helpviewer_keywords: ["IEventTrigger interface [Task Scheduler]","Subscription property","IEventTrigger.Subscription","IEventTrigger.put_Subscription","IEventTrigger::Subscription","IEventTrigger::get_Subscription","IEventTrigger::put_Subscription","Subscription property [Task Scheduler]","Subscription property [Task Scheduler]","IEventTrigger interface","put_Subscription","taskschd.ieventtrigger_subscription","taskschd/IEventTrigger::Subscription","taskschd/IEventTrigger::get_Subscription","taskschd/IEventTrigger::put_Subscription"]
old-location: taskschd\ieventtrigger_subscription.htm
tech.root: taskschd
ms.assetid: 884b98cd-f782-44af-9534-067198a7f48d
ms.date: 12/05/2018
ms.keywords: IEventTrigger interface [Task Scheduler],Subscription property, IEventTrigger.Subscription, IEventTrigger.put_Subscription, IEventTrigger::Subscription, IEventTrigger::get_Subscription, IEventTrigger::put_Subscription, Subscription property [Task Scheduler], Subscription property [Task Scheduler],IEventTrigger interface, put_Subscription, taskschd.ieventtrigger_subscription, taskschd/IEventTrigger::Subscription, taskschd/IEventTrigger::get_Subscription, taskschd/IEventTrigger::put_Subscription
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
 - IEventTrigger::put_Subscription
 - taskschd/IEventTrigger::put_Subscription
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
 - IEventTrigger.Subscription
 - IEventTrigger.get_Subscription
 - IEventTrigger.put_Subscription
---

# IEventTrigger::put_Subscription


## -description

Gets or sets a query string that identifies the event that fires the trigger.

This property is read/write.

## -parameters

## -remarks

When reading or writing your own XML for a task, the event subscription is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-subscription-eventtriggertype-element">Subscription</a> element of the Task Scheduler schema.

For more information about writing a query string for certain events, see <a href="/previous-versions//aa385231(v=vs.85)">Event Selection</a> and <a href="/windows/win32/wes/subscribing-to-events">Subscribing to Events</a>.


#### Examples

The following query string defines a subscription to all level 2 events in the System channel.



```xml
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>"
```

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
