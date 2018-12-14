---
UID: NN:sdoias.ISdoCollection
title: ISdoCollection
author: windows-sdk-content
description: Use the ISdoCollection interface to manipulate a collection of SDO objects.
old-location: nps\SDO_isdocollection.htm
tech.root: Nps
ms.assetid: 26470906-1cba-41fc-96f3-078208ab3d51
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISdoCollection, ISdoCollection interface [Network Policy Server], ISdoCollection interface [Network Policy Server],described, _sdo_isdocollection, nps.SDO_isdocollection, sdo.isdocollection, sdoias/ISdoCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# ISdoCollection interface


## -description


Use the 
<b>ISdoCollection</b> interface to manipulate a collection of SDO objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISdoCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a575b224-9827-47f3-a819-bd793200c901">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57f83f72-327b-4018-be1b-3527820f88d5">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves a count of the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f41211cf-7ed6-4f49-ba90-a72b6eb4db3e">get_NewEnum</a>
</td>
<td align="left" width="63%">
Returns an enumeration interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf9263c3-5d98-4b52-bbd7-6a37fb4c8481">IsNameUnique</a>
</td>
<td align="left" width="63%">
Tests whether an item name is unique in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c830e23-dc6f-49dd-83fe-8ddd39ac1bf6">Item</a>
</td>
<td align="left" width="63%">
Retrieves an item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bf216a0-2d65-4242-97bc-f4b690e92d55">Reload</a>
</td>
<td align="left" width="63%">
Reloads all items in the collection from the underlying datastore.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f390377d-b78e-4548-9602-c0eb363765c7">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82654df4-9a85-4687-86dd-04ea5a916fdc">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
</table> 


## -remarks



To obtain a collection, call 
<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">ISdo::GetProperty</a>, specifying a collection's property. For more information, see 
<a href="https://msdn.microsoft.com/b9090ad5-564c-4f48-b7bd-24617d582d2e">Retrieving a Collection</a>.




## -see-also




<a href="https://msdn.microsoft.com/f529bb20-0e63-424c-8a67-d06f76233d61">Collections</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa">Server Data Objects Interfaces</a>



<a href="https://msdn.microsoft.com/0a73adfb-3f4b-46f6-8b76-d48f8599e05d">Server Data Objects Reference</a>
 

 

