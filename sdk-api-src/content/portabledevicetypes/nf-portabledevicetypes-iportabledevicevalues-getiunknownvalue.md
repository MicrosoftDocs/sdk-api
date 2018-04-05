---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetIUnknownValue
title: IPortableDeviceValues::GetIUnknownValue method
author: windows-driver-content
description: The GetIUnknownValue method retrieves an IUnknown interface value (type VT_UNKNOWN) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getiunknownvalue.htm
old-project: wpd_sdk
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIUnknownValue method [Windows Portable Devices SDK], GetIUnknownValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetIUnknownValue,IPortableDeviceValues.GetIUnknownValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetIUnknownValue method, IPortableDeviceValues::GetIUnknownValue, IPortableDeviceValuesGetIUnknownValue, portabledevicetypes/IPortableDeviceValues::GetIUnknownValue, wpdsdk.iportabledevicevalues_getiunknownvalue
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
-	IPortableDeviceValues.GetIUnknownValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetIUnknownValue method


## -description



The <b>GetIUnknownValue</b> method retrieves an <b>IUnknown</b> interface value (type VT_UNKNOWN) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Address of a variable that receives a pointer to the retrieved <b>IUnknown</b> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.


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
The property specified by <i>key</i> is not an <b>IUnknown</b> interface.

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



<a href="https://msdn.microsoft.com/292adf45-439c-4aae-9b17-e4d9ed701eda">IPortableDeviceValues::SetIUnknownValue</a>
 

 

