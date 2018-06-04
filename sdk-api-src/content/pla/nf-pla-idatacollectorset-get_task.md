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

# IDataCollectorSet::get_Task


## -description


Retrieves or sets the name of a <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> job to start each time the data collector set stops, including between segments.

This property is read/write.


## -parameters


## -remarks



To specify command-line arguments for the task, see <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> and <a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a>. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a>



<a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a>
 

 

