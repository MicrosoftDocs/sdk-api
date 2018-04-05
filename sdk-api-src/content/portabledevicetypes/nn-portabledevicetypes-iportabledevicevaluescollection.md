---
UID: NN:portabledevicetypes.IPortableDeviceValuesCollection
title: IPortableDeviceValuesCollection
author: windows-driver-content
description: The IPortableDeviceValuesCollection interface holds a collection of zero-based indexed IPortableDeviceValues interfaces.
old-location: wpdsdk\iportabledevicevaluescollection.htm
old-project: wpd_sdk
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], described, IPortableDeviceValuesCollectionInterface, portabledevicetypes/IPortableDeviceValuesCollection, wpdsdk.iportabledevicevaluescollection
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
-	IPortableDeviceValuesCollection
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection interface


## -description



The <b>IPortableDeviceValuesCollection</b> interface holds a collection of zero-based indexed <b>IPortableDeviceValues</b> interfaces. This interface can be retrieved from a method, or if a new object is required, call <b>CoCreate</b> with <b>CLSID_PortableDeviceValuesCollection</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceValuesCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceValuesCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceValuesCollection</b> interface has these methods.
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
Adds an item to the collection

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Releases all items from the collection.

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
Retrieves the number of items in the collection.

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
 

 

