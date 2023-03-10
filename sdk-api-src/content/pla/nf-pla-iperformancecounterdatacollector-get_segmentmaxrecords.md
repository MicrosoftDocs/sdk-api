---
UID: NF:pla.IPerformanceCounterDataCollector.get_SegmentMaxRecords
title: IPerformanceCounterDataCollector::get_SegmentMaxRecords (pla.h)
description: Retrieves or sets the maximum number of samples to log. (Get)
helpviewer_keywords: ["IPerformanceCounterDataCollector interface [PLA]","SegmentMaxRecords property","IPerformanceCounterDataCollector.SegmentMaxRecords","IPerformanceCounterDataCollector.get_SegmentMaxRecords","IPerformanceCounterDataCollector::SegmentMaxRecords","IPerformanceCounterDataCollector::get_SegmentMaxRecords","IPerformanceCounterDataCollector::put_SegmentMaxRecords","SegmentMaxRecords property [PLA]","SegmentMaxRecords property [PLA]","IPerformanceCounterDataCollector interface","base.iperformancecounterdatacollector_segmentmaxrecords","get_SegmentMaxRecords","pla.iperformancecounterdatacollector_segmentmaxrecords","pla/IPerformanceCounterDataCollector::SegmentMaxRecords","pla/IPerformanceCounterDataCollector::get_SegmentMaxRecords","pla/IPerformanceCounterDataCollector::put_SegmentMaxRecords"]
old-location: pla\iperformancecounterdatacollector_segmentmaxrecords.htm
tech.root: PLA
ms.assetid: cc987959-dbf6-44da-8f1a-d66a3ad791a5
ms.date: 12/05/2018
ms.keywords: IPerformanceCounterDataCollector interface [PLA],SegmentMaxRecords property, IPerformanceCounterDataCollector.SegmentMaxRecords, IPerformanceCounterDataCollector.get_SegmentMaxRecords, IPerformanceCounterDataCollector::SegmentMaxRecords, IPerformanceCounterDataCollector::get_SegmentMaxRecords, IPerformanceCounterDataCollector::put_SegmentMaxRecords, SegmentMaxRecords property [PLA], SegmentMaxRecords property [PLA],IPerformanceCounterDataCollector interface, base.iperformancecounterdatacollector_segmentmaxrecords, get_SegmentMaxRecords, pla.iperformancecounterdatacollector_segmentmaxrecords, pla/IPerformanceCounterDataCollector::SegmentMaxRecords, pla/IPerformanceCounterDataCollector::get_SegmentMaxRecords, pla/IPerformanceCounterDataCollector::put_SegmentMaxRecords
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
 - IPerformanceCounterDataCollector::get_SegmentMaxRecords
 - pla/IPerformanceCounterDataCollector::get_SegmentMaxRecords
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
 - IPerformanceCounterDataCollector.SegmentMaxRecords
 - IPerformanceCounterDataCollector.get_SegmentMaxRecords
 - IPerformanceCounterDataCollector.put_SegmentMaxRecords
---

# IPerformanceCounterDataCollector::get_SegmentMaxRecords


## -description

Retrieves or sets the maximum number of samples to log.

This property is read/write.

## -parameters

## -remarks

When the maximum number of samples is reached, PLA switches to a new log file and continues logging if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a> property is VARIANT_TRUE; otherwise, PLA stops logging.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a>
