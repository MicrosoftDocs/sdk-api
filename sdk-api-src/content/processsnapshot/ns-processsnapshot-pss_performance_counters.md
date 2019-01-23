---
UID: NS:processsnapshot.__unnamed_struct_7
title: PSS_PERFORMANCE_COUNTERS
author: windows-sdk-content
description: Holds performance counters returned by PssQuerySnapshot.
old-location: proc_snap\pss_performance_counters.htm
tech.root: proc_snap
ms.assetid: 298C1FC8-D19D-4DB3-84AA-3870D06B16A1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSS_PERFORMANCE_COUNTERS, PSS_PERFORMANCE_COUNTERS structure, proc_snap.pss_performance_counters, processsnapshot/PSS_PERFORMANCE_COUNTERS
ms.topic: struct
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_PERFORMANCE_COUNTERS
product: Windows
targetos: Windows
req.typenames: PSS_PERFORMANCE_COUNTERS
req.redist: 
---

# PSS_PERFORMANCE_COUNTERS structure


## -description


Holds performance counters returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field TotalCycleCount

The count of clock cycles spent for capture.


### -field TotalWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for capture.


### -field VaCloneCycleCount

The count of clock cycles spent for the capture of the VA clone.


### -field VaCloneWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for the capture of the VA clone.


### -field VaSpaceCycleCount

The count of clock cycles spent for the capture of VA space information.


### -field VaSpaceWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for the capture VA space information.


### -field AuxPagesCycleCount

The count of clock cycles spent for the capture of auxiliary page information.


### -field AuxPagesWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for the capture of auxiliary page information.


### -field HandlesCycleCount

The count of clock cycles spent for the capture of handle information.


### -field HandlesWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for the capture of handle information.


### -field ThreadsCycleCount

The count of clock cycles spent for the capture of thread information.


### -field ThreadsWallClockPeriod

The count of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> units spent for the capture of thread information.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_PERFORMANCE_COUNTERS</b> structure when the <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_PERFORMANCE_COUNTERS</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

