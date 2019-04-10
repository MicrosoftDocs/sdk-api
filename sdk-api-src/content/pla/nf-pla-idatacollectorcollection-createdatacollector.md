---
UID: NF:pla.IDataCollectorCollection.CreateDataCollector
title: IDataCollectorCollection::CreateDataCollector (pla.h)
author: windows-sdk-content
description: Creates a data collector of the specified type.
old-location: pla\idatacollectorcollection_createdatacollector.htm
tech.root: PLA
ms.assetid: b6d98361-3af3-4fb2-ad0b-4449b81d6e9e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDataCollector, CreateDataCollector method [PLA], CreateDataCollector method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],CreateDataCollector method, IDataCollectorCollection.CreateDataCollector, IDataCollectorCollection::CreateDataCollector, pla.idatacollectorcollection_createdatacollector, pla/IDataCollectorCollection::CreateDataCollector
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
 - IDataCollectorCollection.CreateDataCollector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorCollection::CreateDataCollector


## -description


Creates a data collector of the specified type.


## -parameters




### -param Type [in]

The type of data collector to create. For possible data collector types, see the <a href="https://msdn.microsoft.com/535b17a9-2e71-4513-83be-56a93ab87627">DataCollectorType</a> enumeration.


### -param Collector [out]

An <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> interface of the newly created data collector. To get the actual data collector interface requested, call the <b>QueryInterface</b> method.


## -returns



Returns S_OK if successful.




## -remarks



Use one of the following interface identifiers to query the <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> interface for the specific data collector.

<table>
<tr>
<th>Data collector interface</th>
<th>Interface identifier</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>
</td>
<td>IID_IApiTracingDataCollector</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
</td>
<td>IID_IAlertDataCollector</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a>
</td>
<td>IID_IConfigurationDataCollector</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a>
</td>
<td>IID_IPerformanceCounterDataCollector</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a>
</td>
<td>IID_ITraceDataCollector</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b47fb9d-6ca4-4e6b-b117-027ef1e963ac">IDataCollectorCollection</a>



<a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a>
 

 

