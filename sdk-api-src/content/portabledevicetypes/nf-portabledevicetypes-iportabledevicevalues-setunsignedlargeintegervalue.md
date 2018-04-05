---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetUnsignedLargeIntegerValue
title: IPortableDeviceValues::SetUnsignedLargeIntegerValue method
author: windows-driver-content
description: The SetUnsignedLargeIntegerValue method adds a new ULONGLONG value (type VT_UI8) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setunsignedlargeintegervalue.htm
old-project: wpd_sdk
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetUnsignedLargeIntegerValue method, IPortableDeviceValues::SetUnsignedLargeIntegerValue, IPortableDeviceValuesSetUnsignedLargeIntegerValue, SetUnsignedLargeIntegerValue method [Windows Portable Devices SDK], SetUnsignedLargeIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetUnsignedLargeIntegerValue,IPortableDeviceValues.SetUnsignedLargeIntegerValue, portabledevicetypes/IPortableDeviceValues::SetUnsignedLargeIntegerValue, wpdsdk.iportabledevicevalues_setunsignedlargeintegervalue
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
-	IPortableDeviceValues.SetUnsignedLargeIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetUnsignedLargeIntegerValue method


## -description



The <b>SetUnsignedLargeIntegerValue</b> method adds a new <b>ULONGLONG</b> value (type VT_UI8) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>ULONGLONG</b> that specifies the new value.


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




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/de37c49b-a5f4-424d-8320-1de2d5a624aa">IPortableDeviceValues::GetUnsignedLargeIntegerValue</a>
 

 

