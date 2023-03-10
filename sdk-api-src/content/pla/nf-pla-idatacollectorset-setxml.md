---
UID: NF:pla.IDataCollectorSet.SetXml
title: IDataCollectorSet::SetXml (pla.h)
description: Sets the property values of those properties included in the XML. (IDataCollectorSet.SetXml)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","SetXml method","IDataCollectorSet.SetXml","IDataCollectorSet::SetXml","SetXml","SetXml method [PLA]","SetXml method [PLA]","IDataCollectorSet interface","base.idatacollectorset_setxml","pla.idatacollectorset_setxml","pla/IDataCollectorSet::SetXml"]
old-location: pla\idatacollectorset_setxml.htm
tech.root: PLA
ms.assetid: 10bffd54-990f-412f-baae-b8ab621b02b8
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SetXml method, IDataCollectorSet.SetXml, IDataCollectorSet::SetXml, SetXml, SetXml method [PLA], SetXml method [PLA],IDataCollectorSet interface, base.idatacollectorset_setxml, pla.idatacollectorset_setxml, pla/IDataCollectorSet::SetXml
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
 - IDataCollectorSet::SetXml
 - pla/IDataCollectorSet::SetXml
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
 - IDataCollectorSet.SetXml
---

# IDataCollectorSet::SetXml


## -description

Sets the property values of those properties included in the XML.

## -parameters

### -param xml [in]

XML that contains the properties to set. For details on specifying the XML string, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>.

### -param validation [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">IValueMap::Count</a> property is zero if there were no errors.

## -returns

Returns S_OK if the method call was successful. You must check the value map for errors. If the method returns S_OK	and there are no validation errors, then the set was successfully initialized.

## -remarks

If the XML syntax is valid, this API will return S_OK, even if one or more properties are not valid.  Those properties whose values are valid are set. Those properties whose values are not valid are set to their default value.

To determine the errors that occurred, retrieve the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface for each error. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the XPath of the element in error (for example, /AlertDataCollector/TaskArguments), the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the HRESULT associated with the error, and the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_description">IValueMapItem::Description</a> property contains the message text associated with the error.

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

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-setxml">IDataCollector::SetXml</a>



<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_xml">IDataCollectorSet::Xml</a>
