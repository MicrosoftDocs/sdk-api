---
UID: NF:pla.IDataCollector.SetXml
title: IDataCollector::SetXml
author: windows-sdk-content
description: Sets the property values of those properties included in the XML.
old-location: pla\idatacollector_setxml.htm
tech.root: PLA
ms.assetid: 12ed8697-caec-45d5-9ecf-658b3e4ca8ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollector interface [PLA],SetXml method, IDataCollector.SetXml, IDataCollector::SetXml, SetXml, SetXml method [PLA], SetXml method [PLA],IDataCollector interface, base.idatacollector_setxml, pla.idatacollector_setxml, pla/IDataCollector::SetXml
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
 - IDataCollector.SetXml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollector::SetXml


## -description


Sets the property values of those properties included in the XML. 


## -parameters




### -param Xml [in]

XML that contains the collector properties to set. For details on specifying the XML string, see the Remarks section of <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>.


### -param Validation [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">IValueMap::Count</a> property is zero if there were no errors.


## -returns



Returns S_OK if the method call was successful. You must check the value map for errors. If the method returns S_OK	and there are no validation errors, then the collector was successfully initialized.




## -remarks



If the XML syntax is valid, this API will return S_OK, even if one or more properties are not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

You can also initialize the collector properties by passing the XML to the <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> property when you create the data collector.

The method fails if the collector element specified in the XML does not match the collector type of the interface.

To determine the errors that occurred, retrieve the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface for each error. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the XPath of the element in error  (for example, /AlertDataCollector/TaskArguments), the <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="https://msdn.microsoft.com/ee0669f1-6400-4c32-9f5f-82fd69b7cacd">IValueMapItem::Description</a> property contains the message text associated with the error.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>



<a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a>



<a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a>
 

 

