---
UID: NE:evntrace._ETW_PROCESS_HANDLE_INFO_TYPE
title: ETW_PROCESS_HANDLE_INFO_TYPE (evntrace.h)
description: Specifies what kind of operation will be done on a handle.helpviewer_keywords: ["ETW_PROCESS_HANDLE_INFO_TYPE","ETW_PROCESS_HANDLE_INFO_TYPE enumeration [ETW]","EtwQueryPartitionInformation","EtwQueryProcessHandleInfoMax","etw.etw_process_handle_info_type","evntrace/ETW_PROCESS_HANDLE_INFO_TYPE","evntrace/EtwQueryPartitionInformation","evntrace/EtwQueryProcessHandleInfoMax"]
old-location: etw\etw_process_handle_info_type.htm
tech.root: ETW
ms.assetid: 92932E4C-0A06-4CDE-B14B-BF53226E133B
ms.date: 12/05/2018
ms.keywords: ETW_PROCESS_HANDLE_INFO_TYPE, ETW_PROCESS_HANDLE_INFO_TYPE enumeration [ETW], EtwQueryPartitionInformation, EtwQueryProcessHandleInfoMax, etw.etw_process_handle_info_type, evntrace/ETW_PROCESS_HANDLE_INFO_TYPE, evntrace/EtwQueryPartitionInformation, evntrace/EtwQueryProcessHandleInfoMax
f1_keywords:
- evntrace/ETW_PROCESS_HANDLE_INFO_TYPE
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- evntrace.h
api_name:
- ETW_PROCESS_HANDLE_INFO_TYPE
targetos: Windows
req.typenames: ETW_PROCESS_HANDLE_INFO_TYPE
req.redist: 
ms.custom: 19H1
---

# ETW_PROCESS_HANDLE_INFO_TYPE enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies what kind of operation will be done on a handle. currently used with the <a href="https://docs.microsoft.com/windows/desktop/ETW/querytraceprocessinghandle">QueryTraceProcessingHandle</a> function.


## -enum-fields




### -field EtwQueryPartitionInformation

Used to query partition identifying information.  <i>InBuffer</i> should be Null.  <i>OutBuffer</i> should be large enough to hold the returned <a href="https://docs.microsoft.com/windows/desktop/ETW/etw-trace-partition-information">ETW_TRACE_PARTITION_INFORMATION</a> structure.  Note that this will only return a non-zero structure when the queried handle is for a trace file generated from a non-host partition on Windows 10, version 1709.


### -field EtwQueryProcessHandleInfoMax

Marks the last value in the enumeration for testing purposes.  Should not be used.

