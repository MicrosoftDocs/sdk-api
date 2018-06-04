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

# IDataCollectorSet::put_Segment


## -description


Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment duration is reached before the data collector set is stopped.

This property is read/write.


## -parameters


## -remarks



You would enable segmentation, for example, if you want to write to a new log file when the current log file reaches 100 MB. The name used for the new log is determined by the <a href="https://msdn.microsoft.com/3a7744a6-feb3-4aea-856d-8496aecc0176">IDataCollector::FileNameFormat</a> property. 

The task associated with the data collector set is launched each time a segment is created.

If VARIANT_TRUE, PLA uses both the <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a> and <a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">IDataCollectorSet::SegmentMaxDuration</a> properties, if set, to determine when to segment the log. When one of the limits is reached, PLA segments the log. After segmenting the log, PLA resets the counters for limits.

If VARIANT_FALSE, PLA ignores <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">SegmentMaxSize</a> and <a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">SegmentMaxDuration</a>.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">IDataCollectorSet::SegmentMaxDuration</a>



<a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a>
 

 

