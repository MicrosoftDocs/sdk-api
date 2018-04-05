---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetKeyValue
title: IPortableDeviceValues::GetKeyValue method
author: windows-driver-content
description: The GetKeyValue method retrieves a PROPERTYKEY value specified by a key.
old-location: wpdsdk\iportabledevicevalues_getkeyvalue.htm
old-project: wpd_sdk
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetKeyValue method [Windows Portable Devices SDK], GetKeyValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetKeyValue,IPortableDeviceValues.GetKeyValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetKeyValue method, IPortableDeviceValues::GetKeyValue, IPortableDeviceValuesGetKeyValue, portabledevicetypes/IPortableDeviceValues::GetKeyValue, wpdsdk.iportabledevicevalues_getkeyvalue
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
-	IPortableDeviceValues.GetKeyValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetKeyValue method


## -description



The <b>GetKeyValue</b> method retrieves a <b>PROPERTYKEY</b> value specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>PROPERTYKEY</b> value.


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
The property specified by <i>key</i> is not a <b>PROPERTYKEY</b> type.

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



<a href="https://msdn.microsoft.com/344c52ec-91b1-43f9-b16a-28c24971d805">IPortableDeviceValues::SetKeyValue</a>
 

 

