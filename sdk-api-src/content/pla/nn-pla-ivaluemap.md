---
UID: NN:pla.IValueMap
title: IValueMap (pla.h)
author: windows-sdk-content
description: Manages a collection of name/value pairs.To get this interface, access one of the following properties or methods:IDataCollector::SetXmlIDataCollectorSet::CommitIDataCollectorSet::SetXmlITraceDataProvider::KeywordsAllITraceDataProvider::KeywordsAnyITraceDataProvider::LevelITraceDataProvider::Properties
old-location: pla\ivaluemap.htm
tech.root: PLA
ms.assetid: a7134395-91c6-4ea1-8b76-63830048289f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IValueMap, IValueMap interface [PLA], IValueMap interface [PLA],described, base.ivaluemap, pla.ivaluemap, pla/IValueMap
ms.topic: interface
f1_keywords: 
 - "pla/IValueMap"
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
 - IValueMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IValueMap interface


## -description


Manages a collection of name/value pairs.

To get this interface, access one of the following properties or methods:<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-setxml">IDataCollector::SetXml</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">ITraceDataProvider::KeywordsAll</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">ITraceDataProvider::KeywordsAny</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_level">ITraceDataProvider::Level</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_properties">ITraceDataProvider::Properties</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueMap</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IValueMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IValueMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-addrange">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more items to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-createvaluemapitem">CreateValueMapItem</a>
</td>
<td align="left" width="63%">
Creates a value map item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueMap</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a description of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the requested item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the value of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_valuemaptype">ValueMapType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the type of the items in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a>
 

 

