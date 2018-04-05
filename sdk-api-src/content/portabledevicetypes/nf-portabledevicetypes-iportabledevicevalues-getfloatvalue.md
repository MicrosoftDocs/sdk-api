---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetFloatValue
title: IPortableDeviceValues::GetFloatValue method
author: windows-driver-content
description: The GetFloatValue method retrieves a FLOAT value (type VT_R4) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getfloatvalue.htm
old-project: wpd_sdk
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFloatValue method [Windows Portable Devices SDK], GetFloatValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetFloatValue,IPortableDeviceValues.GetFloatValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetFloatValue method, IPortableDeviceValues::GetFloatValue, IPortableDeviceValuesGetFloatValue, portabledevicetypes/IPortableDeviceValues::GetFloatValue, wpdsdk.iportabledevicevalues_getfloatvalue
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
-	IPortableDeviceValues.GetFloatValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetFloatValue method


## -description



The <b>GetFloatValue</b> method retrieves a <b>FLOAT</b> value (type VT_R4) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>FLOAT</b> value.


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
The property specified by <i>key</i> is not a <b>FLOAT</b> type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not in the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/1e0c9d19-47bf-4d93-a0c0-27e2c4897012">IPortableDeviceValues::SetFloatValue</a>
 

 

