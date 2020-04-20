---
UID: NF:pla.IDataCollectorSet.get_StopOnCompletion
title: IDataCollectorSet::get_StopOnCompletion (pla.h)
description: Retrieves or sets a value that determines whether the data collector set stops when all the data collectors in the set are in a completed state.helpviewer_keywords: ["IDataCollectorSet interface [PLA]","StopOnCompletion property","IDataCollectorSet.StopOnCompletion","IDataCollectorSet.get_StopOnCompletion","IDataCollectorSet::StopOnCompletion","IDataCollectorSet::get_StopOnCompletion","IDataCollectorSet::put_StopOnCompletion","StopOnCompletion property [PLA]","StopOnCompletion property [PLA]","IDataCollectorSet interface","get_StopOnCompletion","pla.idatacollectorset_stoponcompletion","pla/IDataCollectorSet::StopOnCompletion","pla/IDataCollectorSet::get_StopOnCompletion","pla/IDataCollectorSet::put_StopOnCompletion"]
old-location: pla\idatacollectorset_stoponcompletion.htm
tech.root: PLA
ms.assetid: bb7e18c6-e809-455e-9bee-c4bb6cf07c26
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],StopOnCompletion property, IDataCollectorSet.StopOnCompletion, IDataCollectorSet.get_StopOnCompletion, IDataCollectorSet::StopOnCompletion, IDataCollectorSet::get_StopOnCompletion, IDataCollectorSet::put_StopOnCompletion, StopOnCompletion property [PLA], StopOnCompletion property [PLA],IDataCollectorSet interface, get_StopOnCompletion, pla.idatacollectorset_stoponcompletion, pla/IDataCollectorSet::StopOnCompletion, pla/IDataCollectorSet::get_StopOnCompletion, pla/IDataCollectorSet::put_StopOnCompletion
f1_keywords:
- pla/IDataCollectorSet.StopOnCompletion
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
- IDataCollectorSet.StopOnCompletion
- IDataCollectorSet.get_StopOnCompletion
- IDataCollectorSet.put_StopOnCompletion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorSet::get_StopOnCompletion


## -description


Retrieves or sets a value that determines whether the data collector set stops when all the data collectors in the set are in a completed state.

This property is read/write.


## -parameters


## -remarks



A data collector set stops only after all the data collectors in the set are complete. The following table identifies when each data collector is complete.

<table>
<tr>
<th>Collector</th>
<th>Is complete </th>
</tr>
<tr>
<td>Configuration</td>
<td>When all configuration information has been collected.</td>
</tr>
<tr>
<td>Performance Counter and Event Tracing</td>
<td>Immediately if both <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">segment duration</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">segment size</a> are zero. Otherwise, if either segment duration or segment size is specified, then the set completes only after one of the segment conditions is met.For Performance Counter, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-iperformancecounterdatacollector-get_segmentmaxrecords">maximum number of records segment</a> is also considered.

</td>
</tr>
<tr>
<td>Alert and API Tracing</td>
<td>Immediately. </td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-stop">IDataCollectorSet::Stop</a>
 

 

