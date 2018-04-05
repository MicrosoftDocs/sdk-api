---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.GetAt
title: IPortableDevicePropVariantCollection::GetAt method
author: windows-driver-content
description: The GetAt method retrieves an item from the collection by a zero-based index.
old-location: wpdsdk\iportabledevicepropvariantcollection_getat.htm
old-project: wpd_sdk
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAt method [Windows Portable Devices SDK], GetAt method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, GetAt,IPortableDevicePropVariantCollection.GetAt, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], GetAt method, IPortableDevicePropVariantCollection::GetAt, IPortableDevicePropVariantCollectionGetAt, portabledevicetypes/IPortableDevicePropVariantCollection::GetAt, wpdsdk.iportabledevicepropvariantcollection_getat
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
-	IPortableDevicePropVariantCollection.GetAt
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::GetAt method


## -description



The <b>GetAt</b> method retrieves an item from the collection by a zero-based index.




## -parameters




### -param dwIndex [in]

<b>DWORD</b> that contains the zero-based index of the item to retrieve.


### -param pValue [out]

Pointer to a <b>PROPVARIANT</b> structure. The caller is responsible for freeing this memory by calling <b>PropVariantClear</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A required pointer argument was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The index that was passed in was out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>



<a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>



<a href="https://msdn.microsoft.com/1cedb8d9-2476-420c-bab4-c8a032af781b">Retrieving the Content Types Supported by a Device</a>



<a href="https://msdn.microsoft.com/7748e111-9987-4685-8fc8-10c5d4631080">Retrieving the Functional Categories Supported by a Device</a>



<a href="https://msdn.microsoft.com/9a13071a-95a1-4330-92d5-11fa72a8f211">Retrieving the Functional Object Identifiers for a Device</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>



<a href="https://msdn.microsoft.com/0686ba54-4782-42a4-8fdb-2325fc8d8bc2">Setting Properties for Multiple Objects</a>
 

 

