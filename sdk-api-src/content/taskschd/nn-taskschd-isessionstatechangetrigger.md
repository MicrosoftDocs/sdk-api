---
UID: NN:taskschd.ISessionStateChangeTrigger
title: ISessionStateChangeTrigger
author: windows-sdk-content
description: Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.
old-location: taskschd\isessionstatechangetrigger.htm
tech.root: taskschd
ms.assetid: 0bf56d67-6c44-4978-93a9-7b525f2bf140
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISessionStateChangeTrigger, ISessionStateChangeTrigger interface [Task Scheduler], ISessionStateChangeTrigger interface [Task Scheduler],described, taskschd.isessionstatechangetrigger, taskschd/ISessionStateChangeTrigger
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
 - ISessionStateChangeTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISessionStateChangeTrigger interface


## -description


Triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.


## -remarks



When reading or writing your own XML for a task, a session state change trigger is specified using the <a href="https://msdn.microsoft.com/38b0da3c-205f-48c5-83e6-ff7c432c02b9">SessionStateChangeTrigger</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>
 

 

