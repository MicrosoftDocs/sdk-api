---
UID: NF:taskschd.ITaskSettings.put_RunOnlyIfNetworkAvailable
title: ITaskSettings::put_RunOnlyIfNetworkAvailable
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.
old-location: taskschd\itasksettings_runonlyifnetworkavailable.htm
old-project: taskschd
ms.assetid: d0926d75-e7d9-469c-aaa0-ddee8fe22dcd
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RunOnlyIfNetworkAvailable property, ITaskSettings.RunOnlyIfNetworkAvailable, ITaskSettings.put_RunOnlyIfNetworkAvailable, ITaskSettings::RunOnlyIfNetworkAvailable, ITaskSettings::get_RunOnlyIfNetworkAvailable, ITaskSettings::put_RunOnlyIfNetworkAvailable, RunOnlyIfNetworkAvailable property [Task Scheduler], RunOnlyIfNetworkAvailable property [Task Scheduler],ITaskSettings interface, put_RunOnlyIfNetworkAvailable, taskschd.itasksettings_runonlyifnetworkavailable, taskschd/ITaskSettings::RunOnlyIfNetworkAvailable, taskschd/ITaskSettings::get_RunOnlyIfNetworkAvailable, taskschd/ITaskSettings::put_RunOnlyIfNetworkAvailable
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
 - ITaskSettings.RunOnlyIfNetworkAvailable
 - ITaskSettings.get_RunOnlyIfNetworkAvailable
 - ITaskSettings.put_RunOnlyIfNetworkAvailable
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::put_RunOnlyIfNetworkAvailable


## -description


Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.

This property is read/write.


## -parameters


## -remarks



When reading or writing  XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/b7b804d3-b31a-4d70-9ba5-805a285e278e">RunOnlyIfNetworkAvailable</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

