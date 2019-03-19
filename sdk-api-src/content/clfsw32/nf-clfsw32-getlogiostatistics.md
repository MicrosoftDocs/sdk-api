---
UID: NF:clfsw32.GetLogIoStatistics
title: GetLogIoStatistics function (clfsw32.h)
author: windows-sdk-content
description: Retrieves log I/O statistics for a dedicated or multiplexed log that is associated with the specified handle.
old-location: fs\getlogiostatistics.htm
tech.root: Clfs
ms.assetid: 1d4a5486-8a9e-480a-952c-12fc7386af3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLogIoStatistics, GetLogIoStatistics function [Files], clfsw32/GetLogIoStatistics, fs.getlogiostatistics
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - GetLogIoStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLogIoStatistics function


## -description


Retrieves  log I/O statistics for a dedicated or multiplexed log that is associated with the specified handle. This function queries  Common Log File System (CLFS)   for   specific  types of log I/O statistics.  Calling this function on a multiplexed log only associates the statistics with the underlying log.


## -parameters




### -param hLog [in]

A handle to an open log file that <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a> gets.  The log handle can refer to either a dedicated or multiplexed log file.


### -param pvStatsBuffer [in, out]

A pointer to a buffer to receive the I/O statistics.  

This buffer must be at least as large as an I/O statistics packet header. For more information, see  <a href="https://msdn.microsoft.com/ebf3f962-5c15-4caf-910a-13bf02137046">CLFS_IO_STATISTICS_HEADER</a>.


### -param cbStatsBuffer [in]

The size of the I/O statistics buffer <i>pvStatsBuffer</i>, in bytes.   

If the buffer is not large enough for the statistics packet, the function fails with <b>ERROR_MORE_DATA</b>.


### -param eStatsClass [in]

This parameter is not implemented at this time; it is reserved for future use.


### -param pcbStatsWritten [out, optional]

A pointer to a variable to receive the size of the I/O statistics packet that is written to  <i>pvStatsBuffer</i>.   

This value is less than or equal to <i>cbStatsBuffer</i>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/8ba1f5e4-9af3-4c8a-8b57-b6075d0560d6">CLFS_IOSTATS_CLASS</a>



<a href="https://msdn.microsoft.com/ebf3f962-5c15-4caf-910a-13bf02137046">CLFS_IO_STATISTICS_HEADER</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

