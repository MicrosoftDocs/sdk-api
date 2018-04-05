---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
title: IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method
author: windows-driver-content
description: The GetIPortableDevicePropVariantCollectionValue method retrieves an IPortableDevicePropVariantCollection value (type VT_UNKNOWN) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getiportabledevicepropvariantcollectionvalue.htm
old-project: wpd_sdk
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIPortableDevicePropVariantCollectionValue method [Windows Portable Devices SDK], GetIPortableDevicePropVariantCollectionValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetIPortableDevicePropVariantCollectionValue,IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetIPortableDevicePropVariantCollectionValue method, IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue, IPortableDeviceValuesGetIPortableDevicePropVariantCollectionValue, portabledevicetypes/IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue, wpdsdk.iportabledevicevalues_getiportabledevicepropvariantcollectionvalue
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
-	IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method


## -description



The <b>GetIPortableDevicePropVariantCollectionValue</b> method retrieves an <b>IPortableDevicePropVariantCollection</b> value (type VT_UNKNOWN) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Address of a variable that receives a pointer to the retrieved <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.


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
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not an <b>IPortableDevicePropVariantCollection</b> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not in the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3">IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue</a>
 

 

