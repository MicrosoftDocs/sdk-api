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

# __MIDL___MIDL_itf_sysmon_0000_0000_0003 enumeration


## -description


Defines the reason for locking the System Monitor.


## -enum-fields




### -field sysmonBatchNone


### -field sysmonBatchAddFiles


### -field sysmonBatchAddCounters


### -field sysmonBatchAddFilesAutoCounters




#### - SysmonBatchAddCounters

Prevents the System Monitor from sampling the counter immediately when you use <a href="https://msdn.microsoft.com/9daecfe6-c2a9-48af-8b59-4f81f0325535">ICounters.Add</a> to add a counter to the 
collection.


#### - SysmonBatchAddFiles

Prevents the System Monitor from sampling the file immediately when you use <a href="https://msdn.microsoft.com/f6b671ea-9620-49a7-8b0c-0c8e1d9819b0">ILogFiles.Add</a> to add a log file to the 
collection.


#### - SysmonBatchNone

Use to free all locks. Typically, you call <a href="https://msdn.microsoft.com/6b9d683a-7a97-44a4-9eb6-6caaafe2abdd">SystemMonitor.BatchingLock</a> with the same reason you used to gain the lock. For example, if you gained the lock using SysmonBatchAddFiles, you would use SysmonBatchAddFiles when releasing the lock.


## -see-also




<a href="https://msdn.microsoft.com/6b9d683a-7a97-44a4-9eb6-6caaafe2abdd">SystemMonitor.BatchingLock</a>
 

 

