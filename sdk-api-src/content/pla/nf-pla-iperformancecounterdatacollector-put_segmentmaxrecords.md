---
UID: NF:pla.IPerformanceCounterDataCollector.put_SegmentMaxRecords
title: IPerformanceCounterDataCollector::put_SegmentMaxRecords (pla.h)
author: windows-sdk-content
description: Retrieves or sets the maximum number of samples to log.
old-location: pla\iperformancecounterdatacollector_segmentmaxrecords.htm
tech.root: PLA
ms.assetid: cc987959-dbf6-44da-8f1a-d66a3ad791a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPerformanceCounterDataCollector interface [PLA],SegmentMaxRecords property, IPerformanceCounterDataCollector.SegmentMaxRecords, IPerformanceCounterDataCollector.put_SegmentMaxRecords, IPerformanceCounterDataCollector::SegmentMaxRecords, IPerformanceCounterDataCollector::get_SegmentMaxRecords, IPerformanceCounterDataCollector::put_SegmentMaxRecords, SegmentMaxRecords property [PLA], SegmentMaxRecords property [PLA],IPerformanceCounterDataCollector interface, base.iperformancecounterdatacollector_segmentmaxrecords, pla.iperformancecounterdatacollector_segmentmaxrecords, pla/IPerformanceCounterDataCollector::SegmentMaxRecords, pla/IPerformanceCounterDataCollector::get_SegmentMaxRecords, pla/IPerformanceCounterDataCollector::put_SegmentMaxRecords, put_SegmentMaxRecords
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
 - IPerformanceCounterDataCollector.SegmentMaxRecords
 - IPerformanceCounterDataCollector.get_SegmentMaxRecords
 - IPerformanceCounterDataCollector.put_SegmentMaxRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPerformanceCounterDataCollector::put_SegmentMaxRecords


## -description


Retrieves or sets the maximum number of samples to log.

This property is read/write.


## -parameters


## -remarks



When the maximum number of samples is reached, PLA switches to a new log file and continues logging if the <a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a> property is VARIANT_TRUE; otherwise, PLA stops logging.




## -see-also




<a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a>
 

 

