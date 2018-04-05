---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetSignedLargeIntegerValue
title: IPortableDeviceValues::SetSignedLargeIntegerValue method
author: windows-driver-content
description: The SetSignedLargeIntegerValue method adds a new LONGLONG value (type VT_I8) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setsignedlargeintegervalue.htm
old-project: wpd_sdk
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetSignedLargeIntegerValue method, IPortableDeviceValues::SetSignedLargeIntegerValue, IPortableDeviceValuesSetSignedLargeIntegerValue, SetSignedLargeIntegerValue method [Windows Portable Devices SDK], SetSignedLargeIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetSignedLargeIntegerValue,IPortableDeviceValues.SetSignedLargeIntegerValue, portabledevicetypes/IPortableDeviceValues::SetSignedLargeIntegerValue, wpdsdk.iportabledevicevalues_setsignedlargeintegervalue
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
-	IPortableDeviceValues.SetSignedLargeIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetSignedLargeIntegerValue method


## -description



The <b>SetSignedLargeIntegerValue</b> method adds a new <b>LONGLONG</b> value (type VT_I8) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>LONGLONG</b> that specifies the new value.


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



If an existing value has the same key that is specified by the <i>key</i> parameter, it overwrites the existing value without any warning.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/b8d2a0b6-7ca3-4a56-a502-cc18b08df22a">IPortableDeviceValues::GetSignedLargeIntegerValue</a>
 

 

