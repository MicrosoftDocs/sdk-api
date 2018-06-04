---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

