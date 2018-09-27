---
UID: NF:pla.IPerformanceCounterDataCollector.get_DataSourceName
title: IPerformanceCounterDataCollector::get_DataSourceName
author: windows-sdk-content
description: Retrieves or sets the data source name if the log file is an SQL log file.
old-location: pla\iperformancecounterdatacollector_datasourcename.htm
tech.root: PLA
ms.assetid: 67ed9ce6-392b-42ac-81f8-b5f26241c0a8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DataSourceName property [PLA], DataSourceName property [PLA],IPerformanceCounterDataCollector interface, IPerformanceCounterDataCollector interface [PLA],DataSourceName property, IPerformanceCounterDataCollector.DataSourceName, IPerformanceCounterDataCollector.get_DataSourceName, IPerformanceCounterDataCollector::DataSourceName, IPerformanceCounterDataCollector::get_DataSourceName, IPerformanceCounterDataCollector::put_DataSourceName, base.iperformancecounterdatacollector_datasourcename, get_DataSourceName, pla.iperformancecounterdatacollector_datasourcename, pla/IPerformanceCounterDataCollector::DataSourceName, pla/IPerformanceCounterDataCollector::get_DataSourceName, pla/IPerformanceCounterDataCollector::put_DataSourceName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPerformanceCounterDataCollector.DataSourceName
 - IPerformanceCounterDataCollector.get_DataSourceName
 - IPerformanceCounterDataCollector.put_DataSourceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPerformanceCounterDataCollector::get_DataSourceName


## -description


Retrieves or sets the data source name if the log file is an SQL log file.

This property is read/write.


## -parameters


## -remarks



Specify the data source name only if the <a href="https://msdn.microsoft.com/3b980ea6-cb08-4e10-b4b3-40fd504d5e8f">IPerformanceCounterDataCollector::LogFileFormat</a> property is <b>plaSql</b>.




## -see-also




<a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a>
 

 

