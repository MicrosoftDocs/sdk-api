---
UID: NF:portabledevicetypes.IPortableDeviceValuesCollection.GetCount
title: IPortableDeviceValuesCollection::GetCount method
author: windows-driver-content
description: The GetCount method retrieves the number of items in the collection.
old-location: wpdsdk\iportabledevicevaluescollection_getcount.htm
old-project: wpd_sdk
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetCount method [Windows Portable Devices SDK], GetCount method [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface, GetCount,IPortableDeviceValuesCollection.GetCount, IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], GetCount method, IPortableDeviceValuesCollection::GetCount, IPortableDeviceValuesCollectionGetCount, portabledevicetypes/IPortableDeviceValuesCollection::GetCount, wpdsdk.iportabledevicevaluescollection_getcount
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
-	IPortableDeviceValuesCollection.GetCount
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection::GetCount method


## -description



The <b>GetCount</b> method retrieves the number of items in the collection.




## -parameters




### -param pcElems [in]

Pointer to a <b>DWORD</b> that contains the number of <b>IPortableDeviceValues</b> interfaces in the collection.


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




<a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection Interface</a>
 

 

