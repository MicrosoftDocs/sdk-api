---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetErrorValue
title: IPortableDeviceValues::GetErrorValue method
author: windows-driver-content
description: The GetErrorValue method retrieves an HRESULT value (type VT_ERROR) specified by a key.
old-location: wpdsdk\iportabledevicevalues_geterrorvalue.htm
old-project: wpd_sdk
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetErrorValue method [Windows Portable Devices SDK], GetErrorValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetErrorValue,IPortableDeviceValues.GetErrorValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetErrorValue method, IPortableDeviceValues::GetErrorValue, IPortableDeviceValuesGetErrorValue, portabledevicetypes/IPortableDeviceValues::GetErrorValue, wpdsdk.iportabledevicevalues_geterrorvalue
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
-	IPortableDeviceValues.GetErrorValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetErrorValue method


## -description



The <b>GetErrorValue</b> method retrieves an <b>HRESULT</b> value (type VT_ERROR) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>HRESULT</b> value.


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
The property specified by <i>key</i> is not an <b>HRESULT</b> type.

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



<a href="https://msdn.microsoft.com/87369791-42bd-4523-b15a-acf0ea1e5af8">IPortableDeviceValues::SetErrorValue</a>
 

 

