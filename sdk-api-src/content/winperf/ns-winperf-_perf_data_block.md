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

# _PERF_DATA_BLOCK structure


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

Size of this structure, in bytes. You use the header length to find the first <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> structure in the performance data block.


### -field NumObjectTypes

Number of performance objects in the performance data block.


### -field DefaultObject

Reserved.


### -field SystemTime

Time when the system was monitored. This member is in Coordinated Universal Time (UTC) format.


### -field PerfTime

Performance-counter value, in counts, for the system being monitored. For more information, see <a href="_win32_queryperformancecounter_cpp">QueryPerformanceCounter</a>.


### -field PerfFreq

Performance-counter frequency, in counts per second, for the system being monitored. For more information, see <a href="_win32_queryperformancefrequency_cpp">QueryPerformanceFrequency</a>.


### -field PerfTime100nSec

Performance-counter value, in 100 nanosecond units, for the system being monitored. For more information, see <a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a>.


### -field SystemNameLength

Size of the computer name located at <b>SystemNameOffset</b>, in bytes.


### -field SystemNameOffset

Offset from the beginning of this structure to the Unicode name of the computer being monitored. 


## -remarks



The performance data block is returned when a consumer calls <a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a> to retrieve one or more performance objects. This structure is the first structure in the returned block. The next structure in the block is the <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> structure, which defines a performance object. For details on the layout of the performance data block, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

Consumers use <b>PerfTime</b>, <b>PerfFreq</b>, and <b>PerfTime100nSec</b> when calculating counter values unless the counter type contains the <b>PERF_OBJECT_TIMER</b> flag in which case the consumer uses the <b>PerfTime</b> and <b>PerfFreq</b> members of <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>
 

 

