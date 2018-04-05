---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetSignedIntegerValue
title: IPortableDeviceValues::SetSignedIntegerValue method
author: windows-driver-content
description: The SetSignedIntegerValue method adds a new LONG value (type VT_I4) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setsignedintegervalue.htm
old-project: wpd_sdk
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetSignedIntegerValue method, IPortableDeviceValues::SetSignedIntegerValue, IPortableDeviceValuesSetSignedIntegerValue, SetSignedIntegerValue method [Windows Portable Devices SDK], SetSignedIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetSignedIntegerValue,IPortableDeviceValues.SetSignedIntegerValue, portabledevicetypes/IPortableDeviceValues::SetSignedIntegerValue, wpdsdk.iportabledevicevalues_setsignedintegervalue
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
-	IPortableDeviceValues.SetSignedIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetSignedIntegerValue method


## -description



The <b>SetSignedIntegerValue</b> method adds a new <b>LONG</b> value (type VT_I4) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>LONG</b> that specifies the new value.


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



<a href="https://msdn.microsoft.com/d2291a64-d0b3-4a30-a37c-2b6cd9880a11">IPortableDeviceValues::GetSignedIntegerValue</a>
 

 

