---
UID: NF:pla.IDataCollector.SetXml
title: IDataCollector::SetXml (pla.h)
description: Sets the property values of those properties included in the XML. (IDataCollector.SetXml)
helpviewer_keywords: ["IDataCollector interface [PLA]","SetXml method","IDataCollector.SetXml","IDataCollector::SetXml","SetXml","SetXml method [PLA]","SetXml method [PLA]","IDataCollector interface","base.idatacollector_setxml","pla.idatacollector_setxml","pla/IDataCollector::SetXml"]
old-location: pla\idatacollector_setxml.htm
tech.root: PLA
ms.assetid: 12ed8697-caec-45d5-9ecf-658b3e4ca8ba
ms.date: 12/05/2018
ms.keywords: IDataCollector interface [PLA],SetXml method, IDataCollector.SetXml, IDataCollector::SetXml, SetXml, SetXml method [PLA], SetXml method [PLA],IDataCollector interface, base.idatacollector_setxml, pla.idatacollector_setxml, pla/IDataCollector::SetXml
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
 - IDataCollector::SetXml
 - pla/IDataCollector::SetXml
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
 - IDataCollector.SetXml
---

# IDataCollector::SetXml


## -description

Sets the property values of those properties included in the XML.

## -parameters

### -param Xml [in]

XML that contains the collector properties to set. For details on specifying the XML string, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>.

### -param Validation [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">IValueMap::Count</a> property is zero if there were no errors.

## -returns

Returns S_OK if the method call was successful. You must check the value map for errors. If the method returns S_OK	and there are no validation errors, then the collector was successfully initialized.

## -remarks

If the XML syntax is valid, this API will return S_OK, even if one or more properties are not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

You can also initialize the collector properties by passing the XML to the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> property when you create the data collector.

The method fails if the collector element specified in the XML does not match the collector type of the interface.

To determine the errors that occurred, retrieve the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface for each error. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the XPath of the element in error  (for example, /AlertDataCollector/TaskArguments), the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_description">IValueMapItem::Description</a> property contains the message text associated with the error.

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
<td>The property conflicts with another property, for example, both <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">LogAppend</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">LogCircular</a> are VARIANT_TRUE.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a>
