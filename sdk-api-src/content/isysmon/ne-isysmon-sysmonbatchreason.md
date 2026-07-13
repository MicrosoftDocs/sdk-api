---
UID: NE:isysmon.__MIDL___MIDL_itf_sysmon_0000_0000_0003
title: SysmonBatchReason (isysmon.h)
description: Defines the reason for locking the System Monitor.
helpviewer_keywords: ["SysmonBatchAddCounters","SysmonBatchAddFiles","SysmonBatchNone","SysmonBatchReason","SysmonBatchReason enumeration [SysMon]","isysmon/SysmonBatchAddCounters","isysmon/SysmonBatchAddFiles","isysmon/SysmonBatchNone","isysmon/SysmonBatchReason","sysmon.sysmonbatchreason"]
old-location: sysmon\sysmonbatchreason.htm
tech.root: SysMon
ms.assetid: f8dac303-105a-4d83-a92c-7d2002d7e4a3
ms.date: 12/05/2018
ms.keywords: SysmonBatchAddCounters, SysmonBatchAddFiles, SysmonBatchNone, SysmonBatchReason, SysmonBatchReason enumeration [SysMon], isysmon/SysmonBatchAddCounters, isysmon/SysmonBatchAddFiles, isysmon/SysmonBatchNone, isysmon/SysmonBatchReason, sysmon.sysmonbatchreason
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SysmonBatchReason
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_sysmon_0000_0000_0003
 - isysmon/__MIDL___MIDL_itf_sysmon_0000_0000_0003
 - SysmonBatchReason
 - isysmon/SysmonBatchReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ISysmon.h
api_name:
 - SysmonBatchReason
---

## -description

Defines the reason for locking the System Monitor.

## -enum-fields

### -field sysmonBatchNone:0

Use to free all locks. Typically, you call <a href="/windows/desktop/SysMon/systemmonitor-batchinglock">SystemMonitor.BatchingLock</a> with the same reason you used to gain the lock. For example, if you gained the lock using SysmonBatchAddFiles, you would use SysmonBatchAddFiles when releasing the lock.

### -field sysmonBatchAddFiles:1

Prevents the System Monitor from sampling the file immediately when you use <a href="/windows/desktop/SysMon/systemmonitor-logfiles-add">ILogFiles.Add</a> to add a log file to the 
collection.

### -field sysmonBatchAddCounters:2

Prevents the System Monitor from sampling the counter immediately when you use <a href="/windows/desktop/SysMon/counters-add">ICounters.Add</a> to add a counter to the collection.

### -field sysmonBatchAddFilesAutoCounters:3

TBD

## -see-also

<a href="/windows/desktop/SysMon/systemmonitor-batchinglock">SystemMonitor.BatchingLock</a>
