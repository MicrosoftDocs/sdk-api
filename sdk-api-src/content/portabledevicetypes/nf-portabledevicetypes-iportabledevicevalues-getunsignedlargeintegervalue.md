---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetUnsignedLargeIntegerValue
title: IPortableDeviceValues::GetUnsignedLargeIntegerValue method
author: windows-driver-content
description: The GetUnsignedLargeIntegerValue method retrieves a ULONGLONG value (type VT_UI8) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getunsignedlargeintegervalue.htm
old-project: wpd_sdk
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetUnsignedLargeIntegerValue method [Windows Portable Devices SDK], GetUnsignedLargeIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetUnsignedLargeIntegerValue,IPortableDeviceValues.GetUnsignedLargeIntegerValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetUnsignedLargeIntegerValue method, IPortableDeviceValues::GetUnsignedLargeIntegerValue, IPortableDeviceValuesGetUnsignedLargeIntegerValue, portabledevicetypes/IPortableDeviceValues::GetUnsignedLargeIntegerValue, wpdsdk.iportabledevicevalues_getunsignedlargeintegervalue
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
-	IPortableDeviceValues.GetUnsignedLargeIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetUnsignedLargeIntegerValue method


## -description



The <b>GetUnsignedLargeIntegerValue</b> method retrieves a <b>ULONGLONG</b> value (type VT_UI8) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>ULONGLONG</b> value.


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
The property specified by <i>key</i> is not a <b>ULONGLONG</b> type.

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



<a href="https://msdn.microsoft.com/64874b86-7bf1-407a-8fff-a2c07c22f0cb">IPortableDeviceValues::SetUnsignedLargeIntegerValue</a>
 

 

