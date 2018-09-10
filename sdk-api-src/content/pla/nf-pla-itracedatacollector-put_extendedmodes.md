---
UID: NF:pla.ITraceDataCollector.put_ExtendedModes
title: ITraceDataCollector::put_ExtendedModes
author: windows-sdk-content
description: Retrieves or sets the extended log file modes.
old-location: pla\itracedatacollector_extendedmodes.htm
tech.root: PLA
ms.assetid: c9f20dd2-4411-4069-8455-9095939581e8
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ExtendedModes property [PLA], ExtendedModes property [PLA],ITraceDataCollector interface, ITraceDataCollector interface [PLA],ExtendedModes property, ITraceDataCollector.ExtendedModes, ITraceDataCollector.put_ExtendedModes, ITraceDataCollector::ExtendedModes, ITraceDataCollector::get_ExtendedModes, ITraceDataCollector::put_ExtendedModes, base.itracedatacollector_extendedmodes, pla.itracedatacollector_extendedmodes, pla/ITraceDataCollector::ExtendedModes, pla/ITraceDataCollector::get_ExtendedModes, pla/ITraceDataCollector::put_ExtendedModes, put_ExtendedModes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataCollector::put_ExtendedModes


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
For a description of all log file modes and their values, see <a href="https://msdn.microsoft.com/d12aaecb-776a-4476-9ba4-16af30fde9c2">Logging Mode Constants</a>. To set the other available log file modes, set the corresponding PLA property as shown in the following table.

<table>
<tr>
<th>Log file mode</th>
<th>Corresponding PLA property</th>
</tr>
<tr>
<td>EVENT_TRACE_BUFFERING_MODE</td>
<td>
<a href="https://msdn.microsoft.com/eeca98e2-8da1-44e5-8d43-00b52f51bcae">ITraceDataProvider::StreamMode</a> is set to <b>plaBuffering</b>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_APPEND</td>
<td>
<a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">IDataCollector::LogAppend</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_CIRCULAR</td>
<td>
<a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_NEWFILE</td>
<td>
<a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a> and <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_PREALLOCATE</td>
<td>
<a href="https://msdn.microsoft.com/7d05055b-a596-40b0-b289-31641957a72f">ITraceDataCollector::PreallocateFile</a> and <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_FILE_MODE_SEQUENTIAL</td>
<td>
<a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">IDataCollector::LogAppend</a> and <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a> are false.</td>
</tr>
<tr>
<td>EVENT_TRACE_PRIVATE_LOGGER_MODE</td>
<td>
<a href="https://msdn.microsoft.com/63962145-7627-46bc-9be1-3a0738bdb1ce">ITraceDataProvider::ProcessMode</a>.</td>
</tr>
<tr>
<td>EVENT_TRACE_REAL_TIME_MODE</td>
<td>
<a href="https://msdn.microsoft.com/eeca98e2-8da1-44e5-8d43-00b52f51bcae">ITraceDataProvider::StreamMode</a> is set to <b>plaRealTime</b>.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a>
 

 

