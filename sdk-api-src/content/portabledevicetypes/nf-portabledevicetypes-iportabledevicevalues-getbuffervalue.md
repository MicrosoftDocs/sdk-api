---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetBufferValue
title: IPortableDeviceValues::GetBufferValue method
author: windows-driver-content
description: The GetBufferValue method retrieves a byte array value (type VT_VECTOR | VT_UI1) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getbuffervalue.htm
old-project: wpd_sdk
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetBufferValue method [Windows Portable Devices SDK], GetBufferValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetBufferValue,IPortableDeviceValues.GetBufferValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetBufferValue method, IPortableDeviceValues::GetBufferValue, IPortableDeviceValuesGetBufferValue, portabledevicetypes/IPortableDeviceValues::GetBufferValue, wpdsdk.iportabledevicevalues_getbuffervalue
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
-	IPortableDeviceValues.GetBufferValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetBufferValue method


## -description



The <b>GetBufferValue</b> method retrieves a <b>byte array</b> value (type VT_VECTOR | VT_UI1) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Pointer to the retrieved <b>BYTE*</b> value. The caller is responsible for freeing the memory by calling <b>CoTaskMemFree</b>.


### -param pcbValue [out]

Pointer to the size of <i>ppValue</i>, in bytes.


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
The property specified by <i>key</i> is not a <b>BYTE</b>* type.

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
 




## -remarks



Retrieving a <b>NULL</b> buffer or a zero-sized buffer is not supported.






## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/6c421240-2ff8-4862-bd90-1feee5d15a8d">IPortableDeviceValues::SetBufferValue</a>
 

 

