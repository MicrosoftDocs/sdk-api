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

# GetLogIoStatistics function


## -description


Retrieves  log I/O statistics for a dedicated or multiplexed log that is associated with the specified handle. This function queries  Common Log File System (CLFS)   for   specific  types of log I/O statistics.  Calling this function on a multiplexed log only associates the statistics with the underlying log.


## -parameters




### -param hLog [in]

A handle to an open log file that <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a> gets.  The log handle can refer to either a dedicated or multiplexed log file.


### -param pvStatsBuffer [in, out]

A pointer to a buffer to receive the I/O statistics.  

This buffer must be at least as large as an I/O statistics packet header. For more information, see  <a href="https://msdn.microsoft.com/library/windows/hardware/ff541798">CLFS_IO_STATISTICS_HEADER</a>.


### -param cbStatsBuffer [in]

The size of the I/O statistics buffer <i>pvStatsBuffer</i>, in bytes.   

If the buffer is not large enough for the statistics packet, the function fails with <b>ERROR_MORE_DATA</b>.


### -param eStatsClass [in]

This parameter is not implemented at this time; it is reserved for future use.


### -param OPTIONAL

TBD




#### - pcbStatsWritten [out, optional]

A pointer to a variable to receive the size of the I/O statistics packet that is written to  <i>pvStatsBuffer</i>.   

This value is less than or equal to <i>cbStatsBuffer</i>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/8ba1f5e4-9af3-4c8a-8b57-b6075d0560d6">CLFS_IOSTATS_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541798">CLFS_IO_STATISTICS_HEADER</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

