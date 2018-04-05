---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetIPortableDeviceValuesValue
title: IPortableDeviceValues::GetIPortableDeviceValuesValue method
author: windows-driver-content
description: The GetIPortableDeviceValuesValue method retrieves an IPortableDeviceValues value (type VT_UNKNOWN) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getiportabledevicevaluesvalue.htm
old-project: wpd_sdk
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIPortableDeviceValuesValue method [Windows Portable Devices SDK], GetIPortableDeviceValuesValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetIPortableDeviceValuesValue,IPortableDeviceValues.GetIPortableDeviceValuesValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetIPortableDeviceValuesValue method, IPortableDeviceValues::GetIPortableDeviceValuesValue, IPortableDeviceValuesGetIPortableDeviceValuesValue, portabledevicetypes/IPortableDeviceValues::GetIPortableDeviceValuesValue, wpdsdk.iportabledevicevalues_getiportabledevicevaluesvalue
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
-	IPortableDeviceValues.GetIPortableDeviceValuesValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetIPortableDeviceValuesValue method


## -description



The <b>GetIPortableDeviceValuesValue</b> method retrieves an <b>IPortableDeviceValues</b> value (type VT_UNKNOWN) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Address of a variable that receives a pointer to the retrieved <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.


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
The property specified by <i>key</i> is not an <b>IPortableDeviceValues</b> interface.

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



<a href="https://msdn.microsoft.com/3e51964e-6ee0-4885-94ca-cc8000b456b4">IPortableDeviceValues::SetIPortableDeviceValuesValue</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>
 

 

