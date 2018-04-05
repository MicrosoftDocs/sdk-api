---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetSignedIntegerValue
title: IPortableDeviceValues::GetSignedIntegerValue method
author: windows-driver-content
description: The GetSignedIntegerValue method retrieves a LONG value (type VT_I4) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getsignedintegervalue.htm
old-project: wpd_sdk
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetSignedIntegerValue method [Windows Portable Devices SDK], GetSignedIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetSignedIntegerValue,IPortableDeviceValues.GetSignedIntegerValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetSignedIntegerValue method, IPortableDeviceValues::GetSignedIntegerValue, IPortableDeviceValuesGetSignedIntegerValue, portabledevicetypes/IPortableDeviceValues::GetSignedIntegerValue, wpdsdk.iportabledevicevalues_getsignedintegervalue
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
-	IPortableDeviceValues.GetSignedIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetSignedIntegerValue method


## -description



The <b>GetSignedIntegerValue</b> method retrieves a <b>LONG</b> value (type VT_I4) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>LONG</b> value.


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
The property specified by <i>key</i> is not a <b>LONG</b> type.

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



<a href="https://msdn.microsoft.com/b0bb2992-2906-446c-be9a-20bff13f8e1d">IPortableDeviceValues::SetSignedIntegerValue</a>
 

 

