---
UID: NF:mstask.ITaskScheduler.IsOfType
title: ITaskScheduler::IsOfType
author: windows-sdk-content
description: The IsOfType method checks the object's type to verify that it supports a particular interface.
old-location: taskschd\itaskscheduler_isoftype.htm
old-project: TaskSchd
ms.assetid: 6d0a474d-398f-4d85-8e58-5dc2b6283086
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskScheduler interface [Task Scheduler],IsOfType method, ITaskScheduler.IsOfType, ITaskScheduler::IsOfType, IsOfType, IsOfType method [Task Scheduler], IsOfType method [Task Scheduler],ITaskScheduler interface, _msb_itaskscheduler_isoftype, mstask/ITaskScheduler::IsOfType, taskschd.itaskscheduler_isoftype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	ITaskScheduler.IsOfType
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITaskScheduler::IsOfType


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>IsOfType</b> method checks the object's type to verify that it supports a particular interface.


## -parameters




### -param pwszName [in]

A null-terminated string that contains the name of the object to check.


### -param riid [in]

The reference identifier of the interface to be matched.


## -returns



The 
<b>IsOfType</b> method returns S_OK if the object named by <i>pwszName</i> supports the interface specified in <i>riid</i>. Otherwise,  S_FALSE is returned.




## -see-also




<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>
 

 

