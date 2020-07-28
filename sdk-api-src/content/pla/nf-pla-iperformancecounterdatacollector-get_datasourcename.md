---
UID: NF:pla.IPerformanceCounterDataCollector.get_DataSourceName
title: IPerformanceCounterDataCollector::get_DataSourceName (pla.h)
description: Retrieves or sets the data source name if the log file is an SQL log file.
helpviewer_keywords: ["DataSourceName property [PLA]","DataSourceName property [PLA]","IPerformanceCounterDataCollector interface","IPerformanceCounterDataCollector interface [PLA]","DataSourceName property","IPerformanceCounterDataCollector.DataSourceName","IPerformanceCounterDataCollector.get_DataSourceName","IPerformanceCounterDataCollector::DataSourceName","IPerformanceCounterDataCollector::get_DataSourceName","IPerformanceCounterDataCollector::put_DataSourceName","base.iperformancecounterdatacollector_datasourcename","get_DataSourceName","pla.iperformancecounterdatacollector_datasourcename","pla/IPerformanceCounterDataCollector::DataSourceName","pla/IPerformanceCounterDataCollector::get_DataSourceName","pla/IPerformanceCounterDataCollector::put_DataSourceName"]
old-location: pla\iperformancecounterdatacollector_datasourcename.htm
tech.root: PLA
ms.assetid: 67ed9ce6-392b-42ac-81f8-b5f26241c0a8
ms.date: 12/05/2018
ms.keywords: DataSourceName property [PLA], DataSourceName property [PLA],IPerformanceCounterDataCollector interface, IPerformanceCounterDataCollector interface [PLA],DataSourceName property, IPerformanceCounterDataCollector.DataSourceName, IPerformanceCounterDataCollector.get_DataSourceName, IPerformanceCounterDataCollector::DataSourceName, IPerformanceCounterDataCollector::get_DataSourceName, IPerformanceCounterDataCollector::put_DataSourceName, base.iperformancecounterdatacollector_datasourcename, get_DataSourceName, pla.iperformancecounterdatacollector_datasourcename, pla/IPerformanceCounterDataCollector::DataSourceName, pla/IPerformanceCounterDataCollector::get_DataSourceName, pla/IPerformanceCounterDataCollector::put_DataSourceName
f1_keywords:
- pla/IPerformanceCounterDataCollector.DataSourceName
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
- IPerformanceCounterDataCollector.DataSourceName
- IPerformanceCounterDataCollector.get_DataSourceName
- IPerformanceCounterDataCollector.put_DataSourceName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPerformanceCounterDataCollector::get_DataSourceName


## -description


Retrieves or sets the data source name if the log file is an SQL log file.

This property is read/write.


## -parameters


## -remarks



Specify the data source name only if the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-iperformancecounterdatacollector-get_logfileformat">IPerformanceCounterDataCollector::LogFileFormat</a> property is <b>plaSql</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a>
 

 

