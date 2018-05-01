---
UID: NF:pla.IDataCollectorCollection.CreateDataCollectorFromXml
title: IDataCollectorCollection::CreateDataCollectorFromXml method
author: windows-driver-content
description: Creates a data collector using the specified XML.
old-location: pla\idatacollectorcollection_createdatacollectorfromxml.htm
old-project: PLA
ms.assetid: 32a1aba6-24f4-416a-b2ba-9be264fce3fc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateDataCollectorFromXml method [PLA], CreateDataCollectorFromXml method [PLA], IDataCollectorCollection interface, CreateDataCollectorFromXml,IDataCollectorCollection.CreateDataCollectorFromXml, IDataCollectorCollection, IDataCollectorCollection interface [PLA], CreateDataCollectorFromXml method, IDataCollectorCollection::CreateDataCollectorFromXml, pla.idatacollectorcollection_createdatacollectorfromxml, pla/IDataCollectorCollection::CreateDataCollectorFromXml
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorCollection.CreateDataCollectorFromXml
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataCollectorCollection::CreateDataCollectorFromXml method


## -description


Creates a data collector using the specified XML.


## -parameters




### -param bstrXml




### -param pValidation




### -param pCollector






#### - Collector [out]

An <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> interface of the newly created data collector. To get the actual data collector interface requested, call the <b>QueryInterface</b> method.


#### - Validation [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">IValueMap::Count</a> property is zero if there were no errors.


#### - Xml [in]

A string that contains the XML of the data collector to create. For details on specifying the XML string, see the Remarks section of the data collector that you want to create.


## -returns



Returns S_OK if successful.




## -remarks



If the XML syntax is valid, this API will return S_OK, even if one or more properties is not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

To determine the errors that occurred, retrieve the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface for each error. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the XPath of the element in error, for example, /AlertDataCollector/TaskArguments. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="https://msdn.microsoft.com/ee0669f1-6400-4c32-9f5f-82fd69b7cacd">IValueMapItem::Description</a> property contains the message text associated with the error.

Typically, any errors that occur will be one of the following HRESULT values.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>PLA_S_PROPERTY_IGNORED</td>
<td>PLA ignored the property element because the data collector does not contain the specified property.</td>
</tr>
<tr>
<td>PLA_E_PROPERTY_CONFLICT</td>
<td>The property conflicts with another property, for example, both <a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">LogAppend</a> and <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">LogCircular</a> are VARIANT_TRUE.</td>
</tr>
</table>
 

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



<a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a>
 

 

