---
UID: NF:pla.IDataCollectorCollection.CreateDataCollector
title: IDataCollectorCollection::CreateDataCollector (pla.h)
description: Creates a data collector of the specified type.
helpviewer_keywords: ["CreateDataCollector","CreateDataCollector method [PLA]","CreateDataCollector method [PLA]","IDataCollectorCollection interface","IDataCollectorCollection interface [PLA]","CreateDataCollector method","IDataCollectorCollection.CreateDataCollector","IDataCollectorCollection::CreateDataCollector","pla.idatacollectorcollection_createdatacollector","pla/IDataCollectorCollection::CreateDataCollector"]
old-location: pla\idatacollectorcollection_createdatacollector.htm
tech.root: PLA
ms.assetid: b6d98361-3af3-4fb2-ad0b-4449b81d6e9e
ms.date: 12/05/2018
ms.keywords: CreateDataCollector, CreateDataCollector method [PLA], CreateDataCollector method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],CreateDataCollector method, IDataCollectorCollection.CreateDataCollector, IDataCollectorCollection::CreateDataCollector, pla.idatacollectorcollection_createdatacollector, pla/IDataCollectorCollection::CreateDataCollector
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
 - IDataCollectorCollection::CreateDataCollector
 - pla/IDataCollectorCollection::CreateDataCollector
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
 - IDataCollectorCollection.CreateDataCollector
---

# IDataCollectorCollection::CreateDataCollector


## -description

Creates a data collector of the specified type.

## -parameters

### -param Type [in]

The type of data collector to create. For possible data collector types, see the <a href="/windows/win32/api/pla/ne-pla-datacollectortype">DataCollectorType</a> enumeration.

### -param Collector [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> interface of the newly created data collector. To get the actual data collector interface requested, call the <b>QueryInterface</b> method.

## -returns

Returns S_OK if successful.

## -remarks

Use one of the following interface identifiers to query the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> interface for the specific data collector.

<table>
<tr>
<th>Data collector interface</th>
<th>Interface identifier</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a>
</td>
<td>IID_IApiTracingDataCollector</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
</td>
<td>IID_IAlertDataCollector</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>
</td>
<td>IID_IConfigurationDataCollector</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a>
</td>
<td>IID_IPerformanceCounterDataCollector</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>
</td>
<td>IID_ITraceDataCollector</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorcollection">IDataCollectorCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a>