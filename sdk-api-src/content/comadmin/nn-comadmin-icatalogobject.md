---
UID: NN:comadmin.ICatalogObject
title: ICatalogObject
author: windows-sdk-content
description: Represents items in collections on the COM+ catalog. ICatalogObject enables you to get and put properties exposed by objects in the catalog.
old-location: cos\icatalogobject.htm
old-project: cossdk
ms.assetid: fe3f7452-57b2-4f9e-9b48-5dedfe519ac1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICatalogObject, ICatalogObject interface [COM+], ICatalogObject interface [COM+],described, _cos_ICatalogObject_Interface, comadmin/ICatalogObject, cos.icatalogobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comadmin.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
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
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogObject interface


## -description


Represents items in collections on the COM+ catalog. <b>ICatalogObject</b> enables you to get and put properties exposed by objects in the catalog.

The <a href="https://msdn.microsoft.com/en-us/library/ms681193(v=VS.85).aspx">ICatalogCollection::Item</a> method returns a pointer to <b>ICatalogObject</b> when it retrieves an item in the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogObject</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICatalogObject</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms686090(v=VS.85).aspx">IsPropertyReadOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be modified using <a href="https://msdn.microsoft.com/en-us/library/ms687686(v=VS.85).aspx">put_Value</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681176(v=VS.85).aspx">IsPropertyWriteOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be read using <a href="https://msdn.microsoft.com/en-us/library/ms687686(v=VS.85).aspx">get_Value</a>.

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

<a href="https://msdn.microsoft.com/en-us/library/ms679201(v=VS.85).aspx">Key</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms681772(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms686422(v=VS.85).aspx">Valid</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms687686(v=VS.85).aspx">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The value of a named property.

</td>
</tr>
</table> 

