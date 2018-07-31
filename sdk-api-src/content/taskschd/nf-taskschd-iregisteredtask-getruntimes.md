---
UID: NF:taskschd.IRegisteredTask.GetRunTimes
title: IRegisteredTask::GetRunTimes
author: windows-sdk-content
description: Gets the times that the registered task is scheduled to run during a specified time.
old-location: taskschd\iregisteredtask_getruntimes.htm
old-project: TaskSchd
ms.assetid: 3ab41687-085a-414d-8054-9c6fe7439e4e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRunTimes, GetRunTimes method [Task Scheduler], GetRunTimes method [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],GetRunTimes method, IRegisteredTask.GetRunTimes, IRegisteredTask::GetRunTimes, taskschd.iregisteredtask_getruntimes, taskschd/IRegisteredTask::GetRunTimes
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
 - IRegisteredTask.GetRunTimes
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredTask::GetRunTimes


## -description


Gets the times that the registered task is scheduled to run during a specified time.


## -parameters




### -param pstStart [in]

The starting time for the query.


### -param pstEnd [in]

The ending time for the query.


### -param pCount [in, out]

The requested number of runs on input and the returned number of runs on output.


### -param pRunTimes [out]

The scheduled times that the task will run. A <b>NULL</b> LPSYSTEMTIME object should be passed into this parameter. On return, this array contains <i>pCount</i> run times. You must free this array by a calling the <b>CoTaskMemFree</b> function.


## -returns



If the method succeeds, it returns S_OK. If the method returns S_FALSE, the pRunTimes parameter contains pCount items, but there were more runs of the task, that were not returned. Otherwise, it returns an HRESULT error code.




## -remarks



If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

