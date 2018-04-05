---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.Clear
title: IPortableDevicePropVariantCollection::Clear method
author: windows-driver-content
description: The Clear method frees, and then removes, all items from the collection. The collection is considered empty after calling this method.
old-location: wpdsdk\iportabledevicepropvariantcollection_clear.htm
old-project: wpd_sdk
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clear method [Windows Portable Devices SDK], Clear method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, Clear,IPortableDevicePropVariantCollection.Clear, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], Clear method, IPortableDevicePropVariantCollection::Clear, IPortableDevicePropVariantCollectionClear, portabledevicetypes/IPortableDevicePropVariantCollection::Clear, wpdsdk.iportabledevicepropvariantcollection_clear
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IPortableDevicePropVariantCollection.Clear
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::Clear method


## -description



The <b>Clear</b> method frees, and then removes, all items from the collection. The collection is considered empty after calling this method.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



After calling <b>Clear</b>, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting <b>Add</b> operations. A call to <b>Add</b> after calling <b>Clear</b> is considered the "first" <b>Add</b> for this collection.




## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>
 

 

