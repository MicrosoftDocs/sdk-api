---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetAt
title: IPortableDeviceValues::GetAt method
author: windows-driver-content
description: The GetAt method retrieves a value from the collection using the supplied zero-based index.
old-location: wpdsdk\iportabledevicevalues_getat.htm
old-project: wpd_sdk
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAt method [Windows Portable Devices SDK], GetAt method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetAt,IPortableDeviceValues.GetAt, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetAt method, IPortableDeviceValues::GetAt, IPortableDeviceValuesGetAt, portabledevicetypes/IPortableDeviceValues::GetAt, wpdsdk.iportabledevicevalues_getat
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
-	IPortableDeviceValues.GetAt
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetAt method


## -description



The <b>GetAt</b> method retrieves a value from the collection using the supplied zero-based index.




## -parameters




### -param index [in]

A <b>DWORD</b> that specifies a zero-based index in the collection.


### -param pKey [in, out]

An optional <b>PROPERTYKEY</b> pointer that retrieves the key of the specified item.


### -param pValue [in, out]

An optional <b>PROPVARIANT</b> that retrieves the value of the specified item. The caller must free the memory by calling <b>PropVariantClear</b> when done with it.


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
An invalid index number was specified.

</td>
</tr>
</table>
 




## -remarks



If a property indicates a value of type VT_UNKNOWN, the property will be one of the Windows Portable Devices (<a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff597598">IPortableDeviceValuesCollection</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a>). No other interfaces can be returned by Windows Portable Devices.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/c6feecc0-7a06-4f78-9cf1-e2897333b62e">IPortableDeviceValues::GetStringValue</a>
 

 

