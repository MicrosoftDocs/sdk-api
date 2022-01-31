---
UID: NE:processsnapshot.__unnamed_enum_3
title: PSS_QUERY_INFORMATION_CLASS (processsnapshot.h)
description: Specifies what information PssQuerySnapshot function returns.
helpviewer_keywords: ["PSS_QUERY_AUXILIARY_PAGES_INFORMATION","PSS_QUERY_HANDLE_INFORMATION","PSS_QUERY_HANDLE_TRACE_INFORMATION","PSS_QUERY_INFORMATION_CLASS","PSS_QUERY_INFORMATION_CLASS enumeration","PSS_QUERY_PERFORMANCE_COUNTERS","PSS_QUERY_PROCESS_INFORMATION","PSS_QUERY_THREAD_INFORMATION","PSS_QUERY_VA_CLONE_INFORMATION","PSS_QUERY_VA_SPACE_INFORMATION","proc_snap.pss_query_information_class","processsnapshot/PSS_QUERY_AUXILIARY_PAGES_INFORMATION","processsnapshot/PSS_QUERY_HANDLE_INFORMATION","processsnapshot/PSS_QUERY_HANDLE_TRACE_INFORMATION","processsnapshot/PSS_QUERY_INFORMATION_CLASS","processsnapshot/PSS_QUERY_PERFORMANCE_COUNTERS","processsnapshot/PSS_QUERY_PROCESS_INFORMATION","processsnapshot/PSS_QUERY_THREAD_INFORMATION","processsnapshot/PSS_QUERY_VA_CLONE_INFORMATION","processsnapshot/PSS_QUERY_VA_SPACE_INFORMATION"]
old-location: proc_snap\pss_query_information_class.htm
tech.root: proc_snap
ms.assetid: 1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B
ms.date: 12/05/2018
ms.keywords: PSS_QUERY_AUXILIARY_PAGES_INFORMATION, PSS_QUERY_HANDLE_INFORMATION, PSS_QUERY_HANDLE_TRACE_INFORMATION, PSS_QUERY_INFORMATION_CLASS, PSS_QUERY_INFORMATION_CLASS enumeration, PSS_QUERY_PERFORMANCE_COUNTERS, PSS_QUERY_PROCESS_INFORMATION, PSS_QUERY_THREAD_INFORMATION, PSS_QUERY_VA_CLONE_INFORMATION, PSS_QUERY_VA_SPACE_INFORMATION, proc_snap.pss_query_information_class, processsnapshot/PSS_QUERY_AUXILIARY_PAGES_INFORMATION, processsnapshot/PSS_QUERY_HANDLE_INFORMATION, processsnapshot/PSS_QUERY_HANDLE_TRACE_INFORMATION, processsnapshot/PSS_QUERY_INFORMATION_CLASS, processsnapshot/PSS_QUERY_PERFORMANCE_COUNTERS, processsnapshot/PSS_QUERY_PROCESS_INFORMATION, processsnapshot/PSS_QUERY_THREAD_INFORMATION, processsnapshot/PSS_QUERY_VA_CLONE_INFORMATION, processsnapshot/PSS_QUERY_VA_SPACE_INFORMATION
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
req.typenames: PSS_QUERY_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_QUERY_INFORMATION_CLASS
 - processsnapshot/PSS_QUERY_INFORMATION_CLASS
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
 - PSS_QUERY_INFORMATION_CLASS
---

# PSS_QUERY_INFORMATION_CLASS enumeration


## -description

Specifies what information <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> function returns.

## -enum-fields

### -field PSS_QUERY_PROCESS_INFORMATION:0

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_process_information">PSS_PROCESS_INFORMATION</a> structure, with information about the original process.

### -field PSS_QUERY_VA_CLONE_INFORMATION:1

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_va_clone_information">PSS_VA_CLONE_INFORMATION</a> structure, with a handle to the VA clone.

### -field PSS_QUERY_AUXILIARY_PAGES_INFORMATION:2

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_auxiliary_pages_information">PSS_AUXILIARY_PAGES_INFORMATION</a> structure, which contains the count of auxiliary pages captured.

### -field PSS_QUERY_VA_SPACE_INFORMATION:3

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_va_space_information">PSS_VA_SPACE_INFORMATION</a> structure, which contains the count of regions captured.

### -field PSS_QUERY_HANDLE_INFORMATION:4

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_information">PSS_HANDLE_INFORMATION</a> structure, which contains the count of handles captured.

### -field PSS_QUERY_THREAD_INFORMATION:5

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_thread_information">PSS_THREAD_INFORMATION</a> structure, which contains the count of threads captured.

### -field PSS_QUERY_HANDLE_TRACE_INFORMATION:6

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_trace_information">PSS_HANDLE_TRACE_INFORMATION</a> structure, which contains a handle to the handle trace section, and its size.

### -field PSS_QUERY_PERFORMANCE_COUNTERS:7

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_performance_counters">PSS_PERFORMANCE_COUNTERS</a> structure, which contains various performance counters.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
