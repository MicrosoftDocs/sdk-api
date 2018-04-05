---
UID: NF:portabledevicetypes.IPortableDevicePropVariantCollection.GetType
title: IPortableDevicePropVariantCollection::GetType method
author: windows-driver-content
description: The GetType method retrieves the data type of the items in the collection.
old-location: wpdsdk\iportabledevicepropvariantcollection_gettype.htm
old-project: wpd_sdk
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetType method [Windows Portable Devices SDK], GetType method [Windows Portable Devices SDK], IPortableDevicePropVariantCollection interface, GetType,IPortableDevicePropVariantCollection.GetType, IPortableDevicePropVariantCollection, IPortableDevicePropVariantCollection interface [Windows Portable Devices SDK], GetType method, IPortableDevicePropVariantCollection::GetType, IPortableDevicePropVariantCollectionGetType, portabledevicetypes/IPortableDevicePropVariantCollection::GetType, wpdsdk.iportabledevicepropvariantcollection_gettype
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
-	IPortableDevicePropVariantCollection.GetType
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevicePropVariantCollection::GetType method


## -description



The <b>GetType</b> method retrieves the data type of the items in the collection.




## -parameters




### -param pvt [out]

A Platform SDK <b>VARTYPE</b> enumeration value that indicates the data type of all the items in the collection.


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
 




## -remarks



All items that are stored in an <b>IPortableDevicePropVariantCollection</b> are the same type.




## -see-also




<a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection Interface</a>
 

 

