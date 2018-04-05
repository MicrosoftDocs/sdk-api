---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.GetCount
title: IPortableDevicePropVariantCollection::GetCount method
author: windows-driver-content
description: The GetCount method retrieves the number of items in this collection.
old-location: wpdsdk\iportabledevicepropvariantcollection_getcount.htm
old-project: wpd_sdk
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetCount method [Windows Portable Devices SDK], GetCount method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, GetCount,IPortableDevicePropVariantCollection.GetCount, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], GetCount method, IPortableDevicePropVariantCollection::GetCount, IPortableDevicePropVariantCollectionGetCount, portabledevicetypes/IPortableDevicePropVariantCollection::GetCount, wpdsdk.iportabledevicepropvariantcollection_getcount
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
-	IPortableDevicePropVariantCollection.GetCount
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::GetCount method


## -description



The <b>GetCount</b> method retrieves the number of items in this collection.




## -parameters




### -param pcElems [in]

Pointer to a <b>DWORD</b> that contains the number of items in the collection.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>



<a href="https://msdn.microsoft.com/7748e111-9987-4685-8fc8-10c5d4631080">Retrieving the Functional Categories Supported by a Device</a>



<a href="https://msdn.microsoft.com/0686ba54-4782-42a4-8fdb-2325fc8d8bc2">Setting Properties for Multiple Objects</a>
 

 

