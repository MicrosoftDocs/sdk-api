---
UID: NN:taskschd.ISessionStateChangeTrigger
title: ISessionStateChangeTrigger (taskschd.h)
author: windows-sdk-content
description: Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.
old-location: taskschd\isessionstatechangetrigger.htm
tech.root: taskschd
ms.assetid: 0bf56d67-6c44-4978-93a9-7b525f2bf140
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISessionStateChangeTrigger, ISessionStateChangeTrigger interface [Task Scheduler], ISessionStateChangeTrigger interface [Task Scheduler],described, taskschd.isessionstatechangetrigger, taskschd/ISessionStateChangeTrigger
ms.topic: interface
f1_keywords: ["taskschd/ISessionStateChangeTrigger"]
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
 - ISessionStateChangeTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISessionStateChangeTrigger interface


## -description


Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.


## -remarks



When reading or writing your own XML for a task, a session state change trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-sessionstatechangetrigger-triggergroup-element">SessionStateChangeTrigger</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>
 

 

