---
UID: NF:pla.ITraceDataCollector.get_ExtendedModes
title: ITraceDataCollector::get_ExtendedModes (pla.h)
description: Retrieves or sets the extended log file modes. (Get)
helpviewer_keywords: ["ExtendedModes property [PLA]","ExtendedModes property [PLA]","ITraceDataCollector interface","ITraceDataCollector interface [PLA]","ExtendedModes property","ITraceDataCollector.ExtendedModes","ITraceDataCollector.get_ExtendedModes","ITraceDataCollector::ExtendedModes","ITraceDataCollector::get_ExtendedModes","ITraceDataCollector::put_ExtendedModes","base.itracedatacollector_extendedmodes","get_ExtendedModes","pla.itracedatacollector_extendedmodes","pla/ITraceDataCollector::ExtendedModes","pla/ITraceDataCollector::get_ExtendedModes","pla/ITraceDataCollector::put_ExtendedModes"]
old-location: pla\itracedatacollector_extendedmodes.htm
tech.root: PLA
ms.assetid: c9f20dd2-4411-4069-8455-9095939581e8
ms.date: 12/05/2018
ms.keywords: ExtendedModes property [PLA], ExtendedModes property [PLA],ITraceDataCollector interface, ITraceDataCollector interface [PLA],ExtendedModes property, ITraceDataCollector.ExtendedModes, ITraceDataCollector.get_ExtendedModes, ITraceDataCollector::ExtendedModes, ITraceDataCollector::get_ExtendedModes, ITraceDataCollector::put_ExtendedModes, base.itracedatacollector_extendedmodes, get_ExtendedModes, pla.itracedatacollector_extendedmodes, pla/ITraceDataCollector::ExtendedModes, pla/ITraceDataCollector::get_ExtendedModes, pla/ITraceDataCollector::put_ExtendedModes
req.header: pla.h
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceDataCollector::get_ExtendedModes
 - pla/ITraceDataCollector::get_ExtendedModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataCollector.ExtendedModes
 - ITraceDataCollector.get_ExtendedModes
 - ITraceDataCollector.put_ExtendedModes
---

# ITraceDataCollector::get_ExtendedModes


## -description

Retrieves or sets the extended log file modes.

This property is read/write.

## -parameters

## -remarks

 Use this property to set the following log file modes:

<ul>
<li>EVENT_TRACE_PRIVATE_IN_PROC</li>
<li>EVENT_TRACE_USE_GLOBAL_SEQUENCE</li>
<li>EVENT_TRACE_USE_LOCAL_SEQUENCE</li>
<li>EVENT_TRACE_USE_PAGED_MEMORY</li>
</ul>
For a description of all log file modes and their values, see <a href="/windows/desktop/ETW/logging-mode-constants">Logging Mode Constants</a>. To set the other available log file modes, set the corresponding PLA property as shown in the following table.

<table>
<tr>
<th>Log file mode</th>
<th>Corresponding PLA property</th>
</tr>
<tr>
<td>EVENT_TRACE_BUFFERING_MODE</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_streammode">ITraceDataProvider::StreamMode</a> is set to <b>plaBuffering</b>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_APPEND</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">IDataCollector::LogAppend</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_CIRCULAR</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">IDataCollector::LogCircular</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_NEWFILE</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">IDataCollectorSet::SegmentMaxSize</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_PREALLOCATE</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_preallocatefile">ITraceDataCollector::PreallocateFile</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">IDataCollectorSet::SegmentMaxSize</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_SEQUENTIAL</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">IDataCollector::LogAppend</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">IDataCollector::LogCircular</a> are false.</td>
</tr>
<tr>
<td>EVENT_TRACE_PRIVATE_LOGGER_MODE</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_processmode">ITraceDataProvider::ProcessMode</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_REAL_TIME_MODE</td>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_streammode">ITraceDataProvider::StreamMode</a> is set to <b>plaRealTime</b>.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>
