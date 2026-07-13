---
UID: NF:pla.IDataCollectorSet.get_Segment
title: IDataCollectorSet::get_Segment (pla.h)
description: Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment duration is reached before the data collector set is stopped. (Get)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Segment property","IDataCollectorSet.Segment","IDataCollectorSet.get_Segment","IDataCollectorSet::Segment","IDataCollectorSet::get_Segment","IDataCollectorSet::put_Segment","Segment property [PLA]","Segment property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_segment","get_Segment","pla.idatacollectorset_get_segment","pla/IDataCollectorSet::Segment","pla/IDataCollectorSet::get_Segment","pla/IDataCollectorSet::put_Segment"]
old-location: pla\idatacollectorset_get_segment.htm
tech.root: PLA
ms.assetid: 5ecac3dd-0cd1-4563-a6b3-1b98e29fe769
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Segment property, IDataCollectorSet.Segment, IDataCollectorSet.get_Segment, IDataCollectorSet::Segment, IDataCollectorSet::get_Segment, IDataCollectorSet::put_Segment, Segment property [PLA], Segment property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_segment, get_Segment, pla.idatacollectorset_get_segment, pla/IDataCollectorSet::Segment, pla/IDataCollectorSet::get_Segment, pla/IDataCollectorSet::put_Segment
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
 - IDataCollectorSet::get_Segment
 - pla/IDataCollectorSet::get_Segment
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
 - IDataCollectorSet.Segment
 - IDataCollectorSet.get_Segment
 - IDataCollectorSet.put_Segment
---

# IDataCollectorSet::get_Segment


## -description

Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment duration is reached before the data collector set is stopped.

This property is read/write.

## -parameters

## -remarks

You would enable segmentation, for example, if you want to write to a new log file when the current log file reaches 100 MB. The name used for the new log is determined by the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a> property. 

The task associated with the data collector set is launched each time a segment is created.

If VARIANT_TRUE, PLA uses both the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">IDataCollectorSet::SegmentMaxSize</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">IDataCollectorSet::SegmentMaxDuration</a> properties, if set, to determine when to segment the log. When one of the limits is reached, PLA segments the log. After segmenting the log, PLA resets the counters for limits.

If VARIANT_FALSE, PLA ignores <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">SegmentMaxSize</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">SegmentMaxDuration</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">IDataCollectorSet::SegmentMaxDuration</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">IDataCollectorSet::SegmentMaxSize</a>
