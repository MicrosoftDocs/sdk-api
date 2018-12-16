---
UID: NF:pla.IDataCollectorSet.get_Segment
title: IDataCollectorSet::get_Segment
author: windows-sdk-content
description: Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment duration is reached before the data collector set is stopped.
old-location: pla\idatacollectorset_get_segment.htm
tech.root: pla
ms.assetid: 5ecac3dd-0cd1-4563-a6b3-1b98e29fe769
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorSet interface [PLA],Segment property, IDataCollectorSet.Segment, IDataCollectorSet.get_Segment, IDataCollectorSet::Segment, IDataCollectorSet::get_Segment, IDataCollectorSet::put_Segment, Segment property [PLA], Segment property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_segment, get_Segment, pla.idatacollectorset_get_segment, pla/IDataCollectorSet::Segment, pla/IDataCollectorSet::get_Segment, pla/IDataCollectorSet::put_Segment
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
 - IDataCollectorSet.Segment
 - IDataCollectorSet.get_Segment
 - IDataCollectorSet.put_Segment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::get_Segment


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
 

 

