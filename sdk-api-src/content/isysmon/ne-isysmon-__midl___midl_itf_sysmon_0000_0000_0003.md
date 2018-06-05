---
UID: NE:isysmon.__MIDL___MIDL_itf_sysmon_0000_0000_0003
title: "__MIDL___MIDL_itf_sysmon_0000_0000_0003"
author: windows-sdk-content
description: Defines the reason for locking the System Monitor.
old-location: sysmon\sysmonbatchreason.htm
old-project: SysMon
ms.assetid: f8dac303-105a-4d83-a92c-7d2002d7e4a3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SysmonBatchAddCounters, SysmonBatchAddFiles, SysmonBatchNone, SysmonBatchReason, SysmonBatchReason enumeration [SysMon], __MIDL___MIDL_itf_sysmon_0000_0000_0003, isysmon/SysmonBatchAddCounters, isysmon/SysmonBatchAddFiles, isysmon/SysmonBatchNone, isysmon/SysmonBatchReason, sysmon.sysmonbatchreason
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: isysmon.h
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
req.typenames: SysmonBatchReason
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ISysmon.h
api_name:
-	SysmonBatchReason
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

