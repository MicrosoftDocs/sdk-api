---
UID: NF:portabledevicetypes.IPortableDeviceValues.RemoveValue
title: IPortableDeviceValues::RemoveValue method
author: windows-driver-content
description: The RemoveValue method removes an item from the collection.
old-location: wpdsdk\iportabledevicevalues_removevalue.htm
old-project: wpd_sdk
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], RemoveValue method, IPortableDeviceValues::RemoveValue, IPortableDeviceValuesRemoveValue, RemoveValue method [Windows Portable Devices SDK], RemoveValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, RemoveValue,IPortableDeviceValues.RemoveValue, portabledevicetypes/IPortableDeviceValues::RemoveValue, wpdsdk.iportabledevicevalues_removevalue
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
-	IPortableDeviceValues.RemoveValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::RemoveValue method


## -description



The <b>RemoveValue</b> method removes an item from the collection.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to remove.


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
 




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/927844f5-8f57-4596-ae0d-c67b8011ca87">IPortableDeviceValues::GetValue</a>



<a href="https://msdn.microsoft.com/69630a21-79e9-4c96-8ed7-9a41ebb991cd">IPortableDeviceValues::SetValue</a>
 

 

