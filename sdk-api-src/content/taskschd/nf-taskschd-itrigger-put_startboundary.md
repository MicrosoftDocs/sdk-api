---
UID: NF:taskschd.ITrigger.put_StartBoundary
title: ITrigger::put_StartBoundary
author: windows-sdk-content
description: Gets or sets the date and time when the trigger is activated.
old-location: taskschd\itrigger_startboundary.htm
old-project: taskschd
ms.assetid: 749101ae-3db6-44ec-9113-95282c86c3c0
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ITrigger interface [Task Scheduler],StartBoundary property, ITrigger.StartBoundary, ITrigger.put_StartBoundary, ITrigger::StartBoundary, ITrigger::get_StartBoundary, ITrigger::put_StartBoundary, StartBoundary property [Task Scheduler], StartBoundary property [Task Scheduler],ITrigger interface, put_StartBoundary, taskschd.itrigger_startboundary, taskschd/ITrigger::StartBoundary, taskschd/ITrigger::get_StartBoundary, taskschd/ITrigger::put_StartBoundary
ms.prod: windows
ms.technology: windows-sdk
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
 - ITrigger.StartBoundary
 - ITrigger.get_StartBoundary
 - ITrigger.put_StartBoundary
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITrigger::put_StartBoundary


## -description


Gets or sets the date and time when the trigger is activated.

This property is read/write.


## -parameters


## -remarks



The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM. The (+-)HH:MM section of the format defines a certain number of hours and minutes ahead or behind Coordinated Universal Time (UTC). For example the date October 11th, 2005 at 1:21:17 with an offset of eight hours behind UTC would be written as 2005-10-11T13:21:17-08:00. If Z is specified for the UTC offset (for example, 2005-10-11T13:21:17Z), then the no offset from UTC will be used. If you do not specify any offset time or Z for the offset (for example, 2005-10-11T13:21:17), then the time zone and daylight saving information that is set on the local computer will be used.  When an offset is specified (using hours and minutes or Z), then the time and offset are always used regardless of the time zone and daylight saving settings on the local computer.

When reading or writing XML for a task, the trigger start boundary is specified in the  <a href="https://msdn.microsoft.com/95a62ae5-4eba-49df-a25f-0d1181772833">StartBoundary</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

