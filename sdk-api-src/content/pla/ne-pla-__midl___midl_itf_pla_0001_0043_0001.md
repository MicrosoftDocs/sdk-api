---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0001
title: "__MIDL___MIDL_itf_pla_0001_0043_0001"
author: windows-sdk-content
description: Defines the data collector types.
old-location: pla\datacollectortype.htm
tech.root: PLA
ms.assetid: 535b17a9-2e71-4513-83be-56a93ab87627
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DataCollectorType, DataCollectorType enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0001, base.datacollectortype, pla.datacollectortype, pla/DataCollectorType, pla/plaAlert, pla/plaApiTrace, pla/plaConfiguration, pla/plaPerformanceCounter, pla/plaTrace, plaAlert, plaApiTrace, plaConfiguration, plaPerformanceCounter, plaTrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - DataCollectorType
product: Windows
targetos: Windows
req.typenames: DataCollectorType
req.redist: 
---

# __MIDL___MIDL_itf_pla_0001_0043_0001 enumeration


## -description


Defines the data collector types.


## -enum-fields




### -field plaPerformanceCounter

Collects performance counter data. The <a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a> interface represents this data collector.


### -field plaTrace

Collects events from an event trace session. The <a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a> interface represents this data collector.


### -field plaConfiguration

Collects computer configuration information. The <a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a> interface represents this data collector.


### -field plaAlert

Monitors performance counters and performs actions if the counter value crosses the specified threshold. The <a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a> interface represents this data collector.


### -field plaApiTrace

Logs API calls made by the process. The <a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a> interface represents this data collector.


## -see-also




<a href="https://msdn.microsoft.com/a5ec0e60-555c-4a95-b13d-a22cc8db7c28">IDataCollector::DataCollectorType</a>
 

 

