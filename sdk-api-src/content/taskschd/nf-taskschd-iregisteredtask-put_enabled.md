---
UID: NF:taskschd.IRegisteredTask.put_Enabled
title: IRegisteredTask::put_Enabled
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates if the registered task is enabled.
old-location: taskschd\iregisteredtask_enabled.htm
old-project: TaskSchd
ms.assetid: 33486621-3984-4a07-8182-c193847a9f76
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Enabled property [Task Scheduler], Enabled property [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],Enabled property, IRegisteredTask.Enabled, IRegisteredTask.put_Enabled, IRegisteredTask::Enabled, IRegisteredTask::get_Enabled, IRegisteredTask::put_Enabled, put_Enabled, taskschd.iregisteredtask_enabled, taskschd/IRegisteredTask::Enabled, taskschd/IRegisteredTask::get_Enabled, taskschd/IRegisteredTask::put_Enabled
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
 - IRegisteredTask.Enabled
 - IRegisteredTask.get_Enabled
 - IRegisteredTask.put_Enabled
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredTask::put_Enabled


## -description


Gets or sets a Boolean value that indicates if the registered task is enabled.

This property is read/write.


## -parameters


## -remarks



This property is of type VARIANT_BOOL, which uses -1 to specify a true value and 0 to represent false. This property will not return an error if a value other than -1 or 0 is used.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

