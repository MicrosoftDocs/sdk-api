---
UID: NS:processsnapshot.PSS_PERFORMANCE_COUNTERS
title: PSS_PERFORMANCE_COUNTERS (processsnapshot.h)
description: Holds performance counters returned by PssQuerySnapshot.
helpviewer_keywords: ["PSS_PERFORMANCE_COUNTERS","PSS_PERFORMANCE_COUNTERS structure","proc_snap.pss_performance_counters","processsnapshot/PSS_PERFORMANCE_COUNTERS"]
old-location: proc_snap\pss_performance_counters.htm
tech.root: proc_snap
ms.assetid: 298C1FC8-D19D-4DB3-84AA-3870D06B16A1
ms.date: 12/05/2018
ms.keywords: PSS_PERFORMANCE_COUNTERS, PSS_PERFORMANCE_COUNTERS structure, proc_snap.pss_performance_counters, processsnapshot/PSS_PERFORMANCE_COUNTERS
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
targetos: Windows
req.typenames: PSS_PERFORMANCE_COUNTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_PERFORMANCE_COUNTERS
 - processsnapshot/PSS_PERFORMANCE_COUNTERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_PERFORMANCE_COUNTERS
---

# PSS_PERFORMANCE_COUNTERS structure


## -description

Holds performance counters returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a>.

## -struct-fields

### -field TotalCycleCount

The count of clock cycles spent for capture.

### -field TotalWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for capture.

### -field VaCloneCycleCount

The count of clock cycles spent for the capture of the VA clone.

### -field VaCloneWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for the capture of the VA clone.

### -field VaSpaceCycleCount

The count of clock cycles spent for the capture of VA space information.

### -field VaSpaceWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for the capture VA space information.

### -field AuxPagesCycleCount

The count of clock cycles spent for the capture of auxiliary page information.

### -field AuxPagesWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for the capture of auxiliary page information.

### -field HandlesCycleCount

The count of clock cycles spent for the capture of handle information.

### -field HandlesWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for the capture of handle information.

### -field ThreadsCycleCount

The count of clock cycles spent for the capture of thread information.

### -field ThreadsWallClockPeriod

The count of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> units spent for the capture of thread information.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> returns a <b>PSS_PERFORMANCE_COUNTERS</b> structure when the <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_PERFORMANCE_COUNTERS</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

