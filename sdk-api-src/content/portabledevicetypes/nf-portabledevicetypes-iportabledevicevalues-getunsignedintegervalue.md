---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetUnsignedIntegerValue
title: IPortableDeviceValues::GetUnsignedIntegerValue method
author: windows-driver-content
description: The GetUnsignedIntegerValue method retrieves a ULONG value (type VT_UI4) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getunsignedintegervalue.htm
old-project: wpd_sdk
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetUnsignedIntegerValue method [Windows Portable Devices SDK], GetUnsignedIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetUnsignedIntegerValue,IPortableDeviceValues.GetUnsignedIntegerValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetUnsignedIntegerValue method, IPortableDeviceValues::GetUnsignedIntegerValue, IPortableDeviceValuesGetUnsignedIntegerValue, portabledevicetypes/IPortableDeviceValues::GetUnsignedIntegerValue, wpdsdk.iportabledevicevalues_getunsignedintegervalue
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
-	IPortableDeviceValues.GetUnsignedIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetUnsignedIntegerValue method


## -description



The <b>GetUnsignedIntegerValue</b> method retrieves a <b>ULONG</b> value (type VT_UI4) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>ULONG</b> value.


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
The property specified by <i>key</i> is not a <b>ULONG</b> type.

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



<a href="https://msdn.microsoft.com/9b5d1b8c-7863-4807-a34b-56d30a47bd5c">IPortableDeviceValues::SetUnsignedIntegerValue</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>
 

 

