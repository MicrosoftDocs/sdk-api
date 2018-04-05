---
UID: NF:portabledevicetypes.IPortableDeviceValuesCollection.GetAt
title: IPortableDeviceValuesCollection::GetAt method
author: windows-driver-content
description: The GetAt method retrieves an item from the collection by a zero-based index.
old-location: wpdsdk\iportabledevicevaluescollection_getat.htm
old-project: wpd_sdk
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAt method [Windows Portable Devices SDK], GetAt method [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface, GetAt,IPortableDeviceValuesCollection.GetAt, IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], GetAt method, IPortableDeviceValuesCollection::GetAt, IPortableDeviceValuesCollectionGetAt, portabledevicetypes/IPortableDeviceValuesCollection::GetAt, wpdsdk.iportabledevicevaluescollection_getat
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
-	IPortableDeviceValuesCollection.GetAt
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection::GetAt method


## -description



The <b>GetAt</b> method retrieves an item from the collection by a zero-based index.




## -parameters




### -param dwIndex [in]

<b>DWORD</b> that specifies a zero-based index in the collection.


### -param ppValues [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface from the collection. The caller is responsible for calling <b>Release</b> on this interface when done with it.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The zero-based index that was passed in was out of range.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The collection contains a <b>NULL</b> <b>IPortableDeviceValues</b> pointer.

</td>
</tr>
</table>
 




## -remarks



Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.




## -see-also




<a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection Interface</a>
 

 

