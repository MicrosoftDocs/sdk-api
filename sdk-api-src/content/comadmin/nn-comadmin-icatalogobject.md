---
UID: NN:comadmin.ICatalogObject
title: ICatalogObject (comadmin.h)
author: windows-sdk-content
description: Represents items in collections on the COM+ catalog. ICatalogObject enables you to get and put properties exposed by objects in the catalog.
old-location: cos\icatalogobject.htm
tech.root: cossdk
ms.assetid: fe3f7452-57b2-4f9e-9b48-5dedfe519ac1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICatalogObject, ICatalogObject interface [COM+], ICatalogObject interface [COM+],described, _cos_ICatalogObject_Interface, comadmin/ICatalogObject, cos.icatalogobject
ms.topic: interface
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICatalogObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICatalogObject interface


## -description


Represents items in collections on the COM+ catalog. <b>ICatalogObject</b> enables you to get and put properties exposed by objects in the catalog.

The <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_item">ICatalogCollection::Item</a> method returns a pointer to <b>ICatalogObject</b> when it retrieves an item in the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogObject</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICatalogObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICatalogObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-ispropertyreadonly">IsPropertyReadOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be modified using <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_value">put_Value</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-ispropertywriteonly">IsPropertyWriteOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be read using <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_value">get_Value</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogObject</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_key">Key</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The key property of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name property of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_valid">Valid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether all properties were successfully read from the catalog data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_value">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The value of a named property.

</td>
</tr>
</table> 

