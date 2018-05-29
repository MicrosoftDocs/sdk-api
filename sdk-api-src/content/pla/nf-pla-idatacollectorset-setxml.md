---
UID: NF:pla.IDataCollectorSet.SetXml
title: IDataCollectorSet::SetXml
author: windows-sdk-content
description: Sets the property values of those properties included in the XML.
old-location: pla\idatacollectorset_setxml.htm
old-project: PLA
ms.assetid: 10bffd54-990f-412f-baae-b8ab621b02b8
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataCollectorSet interface [PLA],SetXml method, IDataCollectorSet.SetXml, IDataCollectorSet::SetXml, SetXml, SetXml method [PLA], SetXml method [PLA],IDataCollectorSet interface, base.idatacollectorset_setxml, pla.idatacollectorset_setxml, pla/IDataCollectorSet::SetXml
ms.prod: windows
ms.technology: windows-sdk
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
-	IDataCollectorSet.SetXml
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataCollectorSet::SetXml


## -description


Sets the property values of those properties included in the XML.


## -parameters




### -param xml




### -param validation






#### - Xml [in]

XML that contains the properties to set. For details on specifying the XML string, see the Remarks section of <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>.


#### - ppValidation [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">IValueMap::Count</a> property is zero if there were no errors.


## -returns



Returns S_OK if the method call was successful. You must check the value map for errors. If the method returns S_OK	and there are no validation errors, then the set was successfully initialized.




## -remarks



If the XML syntax is valid, this API will return S_OK, even if one or more properties are not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

To determine the errors that occurred, retrieve the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface for each error. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the XPath of the element in error (for example, /AlertDataCollector/TaskArguments), the <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="https://msdn.microsoft.com/ee0669f1-6400-4c32-9f5f-82fd69b7cacd">IValueMapItem::Description</a> property contains the message text associated with the error.

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




<a href="https://msdn.microsoft.com/12ed8697-caec-45d5-9ecf-658b3e4ca8ba">IDataCollector::SetXml</a>



<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/4b07bf1c-58e8-430a-a68c-c16cab954140">IDataCollectorSet::Xml</a>
 

 

