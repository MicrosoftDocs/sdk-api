---
UID: NF:pla.IDataCollectorSet.get_SegmentMaxSize
title: IDataCollectorSet::get_SegmentMaxSize (pla.h)
description: Retrieves or sets the maximum size of any log file in the data collector set. (Get)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","SegmentMaxSize property","IDataCollectorSet.SegmentMaxSize","IDataCollectorSet.get_SegmentMaxSize","IDataCollectorSet::SegmentMaxSize","IDataCollectorSet::get_SegmentMaxSize","IDataCollectorSet::put_SegmentMaxSize","SegmentMaxSize property [PLA]","SegmentMaxSize property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_segmentmaxsize","get_SegmentMaxSize","pla.idatacollectorset_get_segmentmaxsize","pla/IDataCollectorSet::SegmentMaxSize","pla/IDataCollectorSet::get_SegmentMaxSize","pla/IDataCollectorSet::put_SegmentMaxSize"]
old-location: pla\idatacollectorset_get_segmentmaxsize.htm
tech.root: PLA
ms.assetid: 7dd96822-a398-42c3-94f1-b9cd7a647575
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SegmentMaxSize property, IDataCollectorSet.SegmentMaxSize, IDataCollectorSet.get_SegmentMaxSize, IDataCollectorSet::SegmentMaxSize, IDataCollectorSet::get_SegmentMaxSize, IDataCollectorSet::put_SegmentMaxSize, SegmentMaxSize property [PLA], SegmentMaxSize property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_segmentmaxsize, get_SegmentMaxSize, pla.idatacollectorset_get_segmentmaxsize, pla/IDataCollectorSet::SegmentMaxSize, pla/IDataCollectorSet::get_SegmentMaxSize, pla/IDataCollectorSet::put_SegmentMaxSize
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
 - IDataCollectorSet::get_SegmentMaxSize
 - pla/IDataCollectorSet::get_SegmentMaxSize
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
 - IDataCollectorSet.SegmentMaxSize
 - IDataCollectorSet.get_SegmentMaxSize
 - IDataCollectorSet.put_SegmentMaxSize
---

# IDataCollectorSet::get_SegmentMaxSize


## -description

Retrieves or sets the maximum size of any log file in the data collector set.  

This property is read/write.

## -parameters

## -remarks

When the maximum size is reached, PLA creates a new log file to write to if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a> property is enabled.

PLA tries to limit the log file size to this value; however, the actual size of the log file might grow slightly larger than this value.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">IDataCollectorSet::Segment</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">IDataCollectorSet::SegmentMaxDuration</a>
