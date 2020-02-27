---
UID: NF:pla.IDataCollectorSet.put_SegmentMaxDuration
title: IDataCollectorSet::put_SegmentMaxDuration (pla.h)
description: Retrieves or sets the duration that the data collector set can run before it begins writing to new log files.
old-location: pla\idatacollectorset_segmentmaxduration.htm
tech.root: PLA
ms.assetid: d958c7a7-0258-4db6-b650-14a61d59221b
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SegmentMaxDuration property, IDataCollectorSet.SegmentMaxDuration, IDataCollectorSet.put_SegmentMaxDuration, IDataCollectorSet::SegmentMaxDuration, IDataCollectorSet::get_SegmentMaxDuration, IDataCollectorSet::put_SegmentMaxDuration, SegmentMaxDuration property [PLA], SegmentMaxDuration property [PLA],IDataCollectorSet interface, base.idatacollectorset_segmentmaxduration, pla.idatacollectorset_segmentmaxduration, pla/IDataCollectorSet::SegmentMaxDuration, pla/IDataCollectorSet::get_SegmentMaxDuration, pla/IDataCollectorSet::put_SegmentMaxDuration, put_SegmentMaxDuration
f1_keywords:
- pla/IDataCollectorSet.SegmentMaxDuration
dev_langs:
- c++
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
- IDataCollectorSet.SegmentMaxDuration
- IDataCollectorSet.get_SegmentMaxDuration
- IDataCollectorSet.put_SegmentMaxDuration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorSet::put_SegmentMaxDuration


## -description


Retrieves or sets the duration that the data collector set can run before it begins writing to new log files.

This property is read/write.


## -parameters


## -remarks



You must enable the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a> property for this property to take effect.

This duration needs to be less than the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_duration">IDataCollectorSet::Duration</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ischedule-get_enddate">ISchedule::EndDate</a> property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_duration">IDataCollectorSet::Duration</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">IDataCollectorSet::SegmentMaxSize</a>
 

 

