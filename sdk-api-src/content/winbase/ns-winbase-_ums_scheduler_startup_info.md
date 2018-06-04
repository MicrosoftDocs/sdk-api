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

# _UMS_SCHEDULER_STARTUP_INFO structure


## -description


Specifies attributes for a user-mode scheduling (UMS) scheduler thread. The <a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a> function uses this structure.


## -struct-fields




### -field UmsVersion

The UMS version for which the application was built. This parameter must be <b>UMS_VERSION</b>. 


### -field CompletionList

A pointer to a UMS completion list to associate with the calling thread. 


### -field SchedulerProc

A pointer to an application-defined <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a> entry point function. The system calls this function when the calling thread has been converted to UMS and is ready to run UMS worker threads. Subsequently, it calls this function when a UMS worker thread running on the calling thread yields or blocks.


### -field SchedulerParam

An application-defined parameter to pass to the specified <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a> function. 

