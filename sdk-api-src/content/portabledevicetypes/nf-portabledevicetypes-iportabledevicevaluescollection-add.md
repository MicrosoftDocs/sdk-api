---
UID: NF:portabledevicetypes.IPortableDeviceValuesCollection.Add
title: IPortableDeviceValuesCollection::Add method
author: windows-driver-content
description: The Add method adds an item to the collection.
old-location: wpdsdk\iportabledevicevaluescollection_add.htm
old-project: wpd_sdk
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Add method [Windows Portable Devices SDK], Add method [Windows Portable Devices SDK], IPortableDeviceValuesCollection interface, Add,IPortableDeviceValuesCollection.Add, IPortableDeviceValuesCollection, IPortableDeviceValuesCollection interface [Windows Portable Devices SDK], Add method, IPortableDeviceValuesCollection::Add, IPortableDeviceValuesCollectionAdd, portabledevicetypes/IPortableDeviceValuesCollection::Add, wpdsdk.iportabledevicevaluescollection_add
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
-	IPortableDeviceValuesCollection.Add
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValuesCollection::Add method


## -description



The <b>Add</b> method adds an item to the collection.




## -parameters




### -param pValues [in]

Pointer to an <b>IPortableDeviceValues</b> interface to add to the collection. The interface is not actually copied, but <b>AddRef</b> is called on it.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to add the value to the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection Interface</a>
 

 

