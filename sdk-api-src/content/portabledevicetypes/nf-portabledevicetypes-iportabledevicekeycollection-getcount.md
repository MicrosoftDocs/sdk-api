---
UID: NF:portabledevicetypes.IPortableDeviceKeyCollection.GetCount
title: IPortableDeviceKeyCollection::GetCount method
author: windows-driver-content
description: The GetCount method retrieves the number of keys in this collection.
old-location: wpdsdk\iportabledevicekeycollection_getcount.htm
old-project: wpd_sdk
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetCount method [Windows Portable Devices SDK], GetCount method [Windows Portable Devices SDK], IPortableDeviceKeyCollection interface, GetCount,IPortableDeviceKeyCollection.GetCount, IPortableDeviceKeyCollection, IPortableDeviceKeyCollection interface [Windows Portable Devices SDK], GetCount method, IPortableDeviceKeyCollection::GetCount, IPortableDeviceKeyCollectionGetCount, portabledevicetypes/IPortableDeviceKeyCollection::GetCount, wpdsdk.iportabledevicekeycollection_getcount
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
-	IPortableDeviceKeyCollection.GetCount
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceKeyCollection::GetCount method


## -description



The <b>GetCount</b> method retrieves the number of keys in this collection.




## -parameters




### -param pcElems [in]

Pointer to a <b>DWORD</b> that contains the number of keys in the collection.


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




<a href="https://msdn.microsoft.com/2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd">IPortableDeviceKeyCollection Interface</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

