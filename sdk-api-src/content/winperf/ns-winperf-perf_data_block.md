---
UID: NS:winperf._PERF_DATA_BLOCK
title: PERF_DATA_BLOCK (winperf.h)
description: Describes the performance data block that you queried, for example, the number of performance objects returned by the provider and the time-based values that you use when calculating performance values.
helpviewer_keywords: ["*PPERF_DATA_BLOCK","PERF_DATA_BLOCK","PERF_DATA_BLOCK structure [Perf]","_win32_perf_data_block_str","base.perf_data_block_str","perf.perf_data_block_str","winperf/PERF_DATA_BLOCK"]
old-location: perf\perf_data_block_str.htm
tech.root: perf
ms.assetid: 29f89719-7597-4f7b-879e-1670386f8396
ms.date: 12/05/2018
ms.keywords: '*PPERF_DATA_BLOCK, PERF_DATA_BLOCK, PERF_DATA_BLOCK structure [Perf], _win32_perf_data_block_str, base.perf_data_block_str, perf.perf_data_block_str, winperf/PERF_DATA_BLOCK'
req.header: winperf.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PERF_DATA_BLOCK, *PPERF_DATA_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_DATA_BLOCK
 - winperf/_PERF_DATA_BLOCK
 - PPERF_DATA_BLOCK
 - winperf/PPERF_DATA_BLOCK
 - PERF_DATA_BLOCK
 - winperf/PERF_DATA_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winperf.h
api_name:
 - PERF_DATA_BLOCK
---

# PERF_DATA_BLOCK structure


## -description

Describes the performance data block that you queried, for example, the number of performance objects returned by the provider and  the time-based values that you use when calculating performance values.

## -struct-fields

### -field Signature

Array of four wide-characters that contains "PERF".

### -field LittleEndian

Indicates if the counter values are in big endian format or little endian format. If one, the counter values are in little endian format. If zero, the counter values are in big endian format. This value may be zero (big endian format) if you retrieve performance data from a foreign computer, such as a UNIX computer.

### -field Version

Version of the performance structures.

### -field Revision

Revision of the performance structures.

### -field TotalByteLength

Total size of the performance data block, in bytes.

### -field HeaderLength

Size of this structure, in bytes. You use the header length to find the first <a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a> structure in the performance data block.

### -field NumObjectTypes

Number of performance objects in the performance data block.

### -field DefaultObject

Reserved.

### -field SystemTime

Time when the system was monitored. This member is in Coordinated Universal Time (UTC) format.

### -field PerfTime

Performance-counter value, in counts, for the system being monitored. For more information, see <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a>.

### -field PerfFreq

Performance-counter frequency, in counts per second, for the system being monitored. For more information, see <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a>.

### -field PerfTime100nSec

Performance-counter value, in 100 nanosecond units, for the system being monitored. For more information, see <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a>.

### -field SystemNameLength

Size of the computer name located at <b>SystemNameOffset</b>, in bytes.

### -field SystemNameOffset

Offset from the beginning of this structure to the Unicode name of the computer being monitored.

## -remarks

The performance data block is returned when a consumer calls <a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a> to retrieve one or more performance objects. This structure is the first structure in the returned block. The next structure in the block is the <a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a> structure, which defines a performance object. For details on the layout of the performance data block, see <a href="/windows/desktop/PerfCtrs/performance-data-format">Performance Data Format</a>.

Consumers use <b>PerfTime</b>, <b>PerfFreq</b>, and <b>PerfTime100nSec</b> when calculating counter values unless the counter type contains the <b>PERF_OBJECT_TIMER</b> flag in which case the consumer uses the <b>PerfTime</b> and <b>PerfFreq</b> members of <a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a>.

## -see-also

<a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a>



<a href="/windows/desktop/PerfCtrs/performance-data-format">Performance Data Format</a>