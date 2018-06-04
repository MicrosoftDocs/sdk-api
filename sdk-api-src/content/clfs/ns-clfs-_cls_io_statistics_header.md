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

# _CLS_IO_STATISTICS_HEADER structure


## -description


Header for information retrieved by the <a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a> function, which defines the I/O performance counters of a log.


## -struct-fields




### -field ubMajorVersion

The major version of the statistics buffer.


### -field ubMinorVersion

The minor version of the statistics buffer.


### -field eStatsClass

The class of I/O statistics  that is exported. Currently, flush statistics are the only statistics information exported.  These statistics  include the frequency of data and metadata flushes on a dedicated log and the amount of data and metadata flushed. Because  flush statistics are  the  sole statistics class, this member is currently unused but will be used in the future.


### -field cbLength

The length of the statistics buffer, including the header.


### -field coffData

The offset of statistics counters from the beginning of the packet where the statistics data begins.  This field allows transparent modifications to the header and length without affecting  how the statistics data is accessed. 


## -remarks



This header is followed by the I/O statistics counters.




## -see-also




<a href="https://msdn.microsoft.com/8ba1f5e4-9af3-4c8a-8b57-b6075d0560d6">CLFS_IOSTATS_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541794">CLFS_IO_STATISTICS</a>



<a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a>
 

 

