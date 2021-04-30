---
UID: NF:pla.IDataCollectorCollection.CreateDataCollectorFromXml
title: IDataCollectorCollection::CreateDataCollectorFromXml (pla.h)
description: Creates a data collector using the specified XML.
helpviewer_keywords: ["CreateDataCollectorFromXml","CreateDataCollectorFromXml method [PLA]","CreateDataCollectorFromXml method [PLA]","IDataCollectorCollection interface","IDataCollectorCollection interface [PLA]","CreateDataCollectorFromXml method","IDataCollectorCollection.CreateDataCollectorFromXml","IDataCollectorCollection::CreateDataCollectorFromXml","pla.idatacollectorcollection_createdatacollectorfromxml","pla/IDataCollectorCollection::CreateDataCollectorFromXml"]
old-location: pla\idatacollectorcollection_createdatacollectorfromxml.htm
tech.root: PLA
ms.assetid: 32a1aba6-24f4-416a-b2ba-9be264fce3fc
ms.date: 12/05/2018
ms.keywords: CreateDataCollectorFromXml, CreateDataCollectorFromXml method [PLA], CreateDataCollectorFromXml method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],CreateDataCollectorFromXml method, IDataCollectorCollection.CreateDataCollectorFromXml, IDataCollectorCollection::CreateDataCollectorFromXml, pla.idatacollectorcollection_createdatacollectorfromxml, pla/IDataCollectorCollection::CreateDataCollectorFromXml
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
 - IDataCollectorCollection::CreateDataCollectorFromXml
 - pla/IDataCollectorCollection::CreateDataCollectorFromXml
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
 - IDataCollectorCollection.CreateDataCollectorFromXml
---

# IDataCollectorCollection::CreateDataCollectorFromXml


## -description

Creates a data collector using the specified XML.

## -parameters

### -param bstrXml [in]

A string that contains the XML of the data collector to create. For details on specifying the XML string, see the Remarks section of the data collector that you want to create.

### -param pValidation [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">IValueMap::Count</a> property is zero if there were no errors.

### -param pCollector [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> interface of the newly created data collector. To get the actual data collector interface requested, call the <b>QueryInterface</b> method.

## -returns

Returns S_OK if successful.

## -remarks

If the XML syntax is valid, this API will return S_OK, even if one or more properties is not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

To determine the errors that occurred, retrieve the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface for each error. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the XPath of the element in error, for example, /AlertDataCollector/TaskArguments. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_description">IValueMapItem::Description</a> property contains the message text associated with the error.

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



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollector">IDataCollectorCollection::CreateDataCollector</a>