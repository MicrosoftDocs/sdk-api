---
UID: NN:taskschd.ISessionStateChangeTrigger
title: ISessionStateChangeTrigger (taskschd.h)
description: Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.
helpviewer_keywords: ["ISessionStateChangeTrigger","ISessionStateChangeTrigger interface [Task Scheduler]","ISessionStateChangeTrigger interface [Task Scheduler]","described","taskschd.isessionstatechangetrigger","taskschd/ISessionStateChangeTrigger"]
old-location: taskschd\isessionstatechangetrigger.htm
tech.root: taskschd
ms.assetid: 0bf56d67-6c44-4978-93a9-7b525f2bf140
ms.date: 12/05/2018
ms.keywords: ISessionStateChangeTrigger, ISessionStateChangeTrigger interface [Task Scheduler], ISessionStateChangeTrigger interface [Task Scheduler],described, taskschd.isessionstatechangetrigger, taskschd/ISessionStateChangeTrigger
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
 - ISessionStateChangeTrigger
 - taskschd/ISessionStateChangeTrigger
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
 - ISessionStateChangeTrigger
---

# ISessionStateChangeTrigger interface


## -description

Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.

## -remarks

When reading or writing your own XML for a task, a session state change trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-sessionstatechangetrigger-triggergroup-element">SessionStateChangeTrigger</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>