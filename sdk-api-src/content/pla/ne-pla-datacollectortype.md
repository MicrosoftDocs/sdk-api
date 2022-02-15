---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0001
title: DataCollectorType (pla.h)
description: Defines the data collector types.
helpviewer_keywords: ["DataCollectorType","DataCollectorType enumeration [PLA]","base.datacollectortype","pla.datacollectortype","pla/DataCollectorType","pla/plaAlert","pla/plaApiTrace","pla/plaConfiguration","pla/plaPerformanceCounter","pla/plaTrace","plaAlert","plaApiTrace","plaConfiguration","plaPerformanceCounter","plaTrace"]
old-location: pla\datacollectortype.htm
tech.root: PLA
ms.assetid: 535b17a9-2e71-4513-83be-56a93ab87627
ms.date: 12/05/2018
ms.keywords: DataCollectorType, DataCollectorType enumeration [PLA], base.datacollectortype, pla.datacollectortype, pla/DataCollectorType, pla/plaAlert, pla/plaApiTrace, pla/plaConfiguration, pla/plaPerformanceCounter, pla/plaTrace, plaAlert, plaApiTrace, plaConfiguration, plaPerformanceCounter, plaTrace
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DataCollectorType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0001
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0001
 - DataCollectorType
 - pla/DataCollectorType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - DataCollectorType
---

# DataCollectorType enumeration


## -description

Defines the data collector types.

## -enum-fields

### -field plaPerformanceCounter:0

Collects performance counter data. The <a href="/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a> interface represents this data collector.

### -field plaTrace:1

Collects events from an event trace session. The <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a> interface represents this data collector.

### -field plaConfiguration:2

Collects computer configuration information. The <a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a> interface represents this data collector.

### -field plaAlert:3

Monitors performance counters and performs actions if the counter value crosses the specified threshold. The <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a> interface represents this data collector.

### -field plaApiTrace:4

Logs API calls made by the process. The <a href="/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a> interface represents this data collector.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_datacollectortype">IDataCollector::DataCollectorType</a>
