---
UID: NF:taskschd.ILogonTrigger.put_UserId
title: ILogonTrigger::put_UserId (taskschd.h)
description: Gets or sets the identifier of the user. (Put)
helpviewer_keywords: ["ILogonTrigger interface [Task Scheduler]","UserId property","ILogonTrigger.UserId","ILogonTrigger.put_UserId","ILogonTrigger::UserId","ILogonTrigger::get_UserId","ILogonTrigger::put_UserId","UserId property [Task Scheduler]","UserId property [Task Scheduler]","ILogonTrigger interface","put_UserId","taskschd.ilogontrigger_userid","taskschd/ILogonTrigger::UserId","taskschd/ILogonTrigger::get_UserId","taskschd/ILogonTrigger::put_UserId"]
old-location: taskschd\ilogontrigger_userid.htm
tech.root: taskschd
ms.assetid: 22d69609-1400-41eb-ae25-4ca05c4733ba
ms.date: 12/05/2018
ms.keywords: ILogonTrigger interface [Task Scheduler],UserId property, ILogonTrigger.UserId, ILogonTrigger.put_UserId, ILogonTrigger::UserId, ILogonTrigger::get_UserId, ILogonTrigger::put_UserId, UserId property [Task Scheduler], UserId property [Task Scheduler],ILogonTrigger interface, put_UserId, taskschd.ilogontrigger_userid, taskschd/ILogonTrigger::UserId, taskschd/ILogonTrigger::get_UserId, taskschd/ILogonTrigger::put_UserId
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
 - ILogonTrigger::put_UserId
 - taskschd/ILogonTrigger::put_UserId
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
 - ILogonTrigger.UserId
 - ILogonTrigger.get_UserId
 - ILogonTrigger.put_UserId
---

# ILogonTrigger::put_UserId


## -description

Gets or sets the identifier of the user.

This property is read/write.

## -parameters

## -remarks

If you want a task to be triggered when any member of a group logs on to the computer rather than when  a specific user logs on, then do not assign a value to the  <b>UserId</b> property.  Instead, create a logon trigger with an empty <b>UserId</b> property and assign a value to the principal for the task using the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid">GroupId</a> property.

When reading or writing XML for a task, the logon user identifier is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-userid-logontriggertype-element">UserId</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger">ILogonTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
