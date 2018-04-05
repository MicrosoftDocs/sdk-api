---
UID: NF:portabledevicetypes.IPortableDeviceValuesCollection.Clear
title: IPortableDeviceValuesCollection::Clear method
author: windows-driver-content
description: The Clear method releases all items from the collection.
old-location: wpdsdk\iportabledevicevaluescollection_clear.htm
old-project: wpd_sdk
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clear method [Windows Portable Devices SDK], Clear method [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface, Clear,IPortableDeviceValuesCollection.Clear, IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], Clear method, IPortableDeviceValuesCollection::Clear, IPortableDeviceValuesCollectionClear, portabledevicetypes/IPortableDeviceValuesCollection::Clear, wpdsdk.iportabledevicevaluescollection_clear
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
-	IPortableDeviceValuesCollection.Clear
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection::Clear method


## -description



The <b>Clear</b> method releases all items from the collection.




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



The method releases all memory that is allocated for the items in the collection.




## -see-also




<a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection Interface</a>
 

 

