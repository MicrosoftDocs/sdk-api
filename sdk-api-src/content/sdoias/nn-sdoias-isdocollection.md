---
UID: NN:sdoias.ISdoCollection
title: ISdoCollection (sdoias.h)
author: windows-sdk-content
description: Use the ISdoCollection interface to manipulate a collection of SDO objects.
old-location: nps\SDO_isdocollection.htm
tech.root: Nps
ms.assetid: 26470906-1cba-41fc-96f3-078208ab3d51
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISdoCollection, ISdoCollection interface [Network Policy Server], ISdoCollection interface [Network Policy Server],described, _sdo_isdocollection, nps.SDO_isdocollection, sdo.isdocollection, sdoias/ISdoCollection
ms.topic: interface
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoCollection interface


## -description


Use the 
<b>ISdoCollection</b> interface to manipulate a collection of SDO objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdoCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdoCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves a count of the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-get__newenum">get_NewEnum</a>
</td>
<td align="left" width="63%">
Returns an enumeration interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique">IsNameUnique</a>
</td>
<td align="left" width="63%">
Tests whether an item name is unique in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves an item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-reload">Reload</a>
</td>
<td align="left" width="63%">
Reloads all items in the collection from the underlying datastore.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdocollection-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
</table> 


## -remarks



To obtain a collection, call 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty">ISdo::GetProperty</a>, specifying a collection's property. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-retrieving-a-collection">Retrieving a Collection</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-collections">Collections</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data Objects Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data Objects Reference</a>
 

 

