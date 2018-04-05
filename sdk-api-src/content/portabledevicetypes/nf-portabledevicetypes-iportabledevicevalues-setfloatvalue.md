---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetFloatValue
title: IPortableDeviceValues::SetFloatValue method
author: windows-driver-content
description: The SetFloatValue method adds a new FLOAT value (type VT_R4) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setfloatvalue.htm
old-project: wpd_sdk
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetFloatValue method, IPortableDeviceValues::SetFloatValue, IPortableDeviceValuesSetFloatValue, SetFloatValue method [Windows Portable Devices SDK], SetFloatValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetFloatValue,IPortableDeviceValues.SetFloatValue, portabledevicetypes/IPortableDeviceValues::SetFloatValue, wpdsdk.iportabledevicevalues_setfloatvalue
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
-	IPortableDeviceValues.SetFloatValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetFloatValue method


## -description



The <b>SetFloatValue</b> method adds a new <b>FLOAT</b> value (type VT_R4) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>FLOAT</b> that contains the new value.


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



<a href="https://msdn.microsoft.com/8a134dfb-f671-4cde-ae35-c8a41be270cf">IPortableDeviceValues::GetFloatValue</a>
 

 

