---
UID: NN:portabledevicetypes.IPortableDevicePropVariantCollection
title: IPortableDevicePropVariantCollection
author: windows-driver-content
description: The IPortableDevicePropVariantCollection interface holds a collection of indexed PROPVARIANT values of the same VARTYPE.
old-location: wpdsdk\iportabledevicepropvariantcollection.htm
old-project: wpd_sdk
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], described, IPortableDevicePropVariantCollectionInterface, portabledevicetypes/IPortableDevicePropVariantCollection, wpdsdk.iportabledevicepropvariantcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portabledevicetypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_STREAM_UNITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevicePropVariantCollection
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection interface


## -description



The <b>IPortableDevicePropVariantCollection</b> interface holds a collection of indexed <b>PROPVARIANT</b> values of the same VARTYPE. The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection. An attempt to add an item of a different VARTYPE may fail if the <b>PROPVARIANT</b> value cannot be changed to the collection's current VARTYPE. To change the VARTYPE of the collection, call <b>ChangeType</b>.

This interface can be retrieved from a method or, if a new object is required, call <b>CoCreate</b> with <b>CLSID_PortableDevicePropVariantCollection</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevicePropVariantCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDevicePropVariantCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDevicePropVariantCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597591">ChangeType</a>
</td>
<td align="left" width="63%">
Converts all items in the collection to the specified VARTYPE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Frees, and then removes, all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Retrieves an item from the collection by a zero-based index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in this collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of the items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597596">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes the element stored at the location specified by the given index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597553">Collection Interfaces</a>
 

 

