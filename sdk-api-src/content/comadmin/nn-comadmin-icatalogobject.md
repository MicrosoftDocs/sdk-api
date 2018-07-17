---
UID: NN:comadmin.ICatalogObject
title: ICatalogObject
author: windows-sdk-content
description: Represents items in collections on the COM+ catalog. ICatalogObject enables you to get and put properties exposed by objects in the catalog.
old-location: cos\icatalogobject.htm
old-project: cossdk
ms.assetid: fe3f7452-57b2-4f9e-9b48-5dedfe519ac1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICatalogObject, ICatalogObject interface [COM+], ICatalogObject interface [COM+],described, _cos_ICatalogObject_Interface, comadmin/ICatalogObject, cos.icatalogobject
ms.prod: windows
ms.technology: windows-sdk
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

The <a href="https://msdn.microsoft.com/47c9dcfd-81fc-495c-848a-8c2b655e8fce">ICatalogCollection::Item</a> method returns a pointer to <b>ICatalogObject</b> when it retrieves an item in the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogObject</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICatalogObject</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bd088794-1245-4cb8-a1f7-385354640675">IsPropertyReadOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be modified using <a href="https://msdn.microsoft.com/eb4203c5-b51c-411c-9c2d-405b3d70bc80">put_Value</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/463ca1eb-5386-4265-882b-fa29c4cbe877">IsPropertyWriteOnly</a>
</td>
<td align="left" width="63%">
Indicates whether the specified property can be read using <a href="https://msdn.microsoft.com/eb4203c5-b51c-411c-9c2d-405b3d70bc80">get_Value</a>.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895751">Key</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/c2fdeae4-e8f0-45c1-b42a-0bd088c26d6f">Valid</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The value of a named property.

</td>
</tr>
</table> 

