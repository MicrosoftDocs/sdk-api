---
UID: NF:portabledevicetypes.IPortableDeviceValuesCollection.RemoveAt
title: IPortableDeviceValuesCollection::RemoveAt method
author: windows-driver-content
description: The RemoveAt method removes the element stored at the location specified by the given index.
old-location: wpdsdk\iportabledevicevaluescollection_removeat.htm
old-project: wpd_sdk
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], RemoveAt method, IPortableDeviceValuesCollection::RemoveAt, IPortableDeviceValuesCollectionRemoveAt, RemoveAt method [Windows Portable Devices SDK], RemoveAt method [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface, RemoveAt,IPortableDeviceValuesCollection.RemoveAt, portabledevicetypes/IPortableDeviceValuesCollection::RemoveAt, wpdsdk.iportabledevicevaluescollection_removeat
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
-	IPortableDeviceValuesCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection::RemoveAt method


## -description



The <b>RemoveAt</b> method removes the element stored at the location specified by the given index.




## -parameters




### -param dwIndex [in]

Specifies the index of the element to be removed.


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
The specified index was out of range.

</td>
</tr>
</table>
 




## -remarks



You must specify a zero-based index.




## -see-also




<a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection Interface</a>
 

 

