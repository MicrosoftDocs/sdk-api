---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetStringValue
title: IPortableDeviceValues::GetStringValue method
author: windows-driver-content
description: The GetStringValue method retrieves a string value (type VT_LPWSTR) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getstringvalue.htm
old-project: wpd_sdk
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetStringValue method [Windows Portable Devices SDK], GetStringValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetStringValue,IPortableDeviceValues.GetStringValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetStringValue method, IPortableDeviceValues::GetStringValue, IPortableDeviceValuesGetStringValue, portabledevicetypes/IPortableDeviceValues::GetStringValue, wpdsdk.iportabledevicevalues_getstringvalue
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
-	IPortableDeviceValues.GetStringValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetStringValue method


## -description



The <b>GetStringValue</b> method retrieves a string value (type VT_LPWSTR) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>LPWSTR</b> value. The caller is responsible for calling <b>CoTaskMemFree</b> to release the memory.


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
The property specified by <i>key</i> is not an <b>LPWSTR</b> type.

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



<a href="https://msdn.microsoft.com/d52675f0-55b4-43ef-bb1d-ff6aa8a70647">IPortableDeviceValues::GetAt</a>



<a href="https://msdn.microsoft.com/a6eba2b9-de18-431e-874e-af68695e8d3f">IPortableDeviceValues::SetStringValue</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

