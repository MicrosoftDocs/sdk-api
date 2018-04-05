---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
title: IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method
author: windows-driver-content
description: The GetIPortableDeviceKeyCollectionValue method retrieves an IPortableDeviceKeyCollection value (type VT_UNKNOWN) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getiportabledevicekeycollectionvalue.htm
old-project: wpd_sdk
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIPortableDeviceKeyCollectionValue method [Windows Portable Devices SDK], GetIPortableDeviceKeyCollectionValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetIPortableDeviceKeyCollectionValue,IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetIPortableDeviceKeyCollectionValue method, IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue, IPortableDeviceValuesGetIPortableDeviceKeyCollectionValue, portabledevicetypes/IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue, wpdsdk.iportabledevicevalues_getiportabledevicekeycollectionvalue
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
-	IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method


## -description



The <b>GetIPortableDeviceKeyCollectionValue</b> method retrieves an <b>IPortableDeviceKeyCollection</b> value (type VT_UNKNOWN) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Pointer to the retrieved <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface pointer. The caller is responsible for calling <b>Release</b> on the retrieved interface.


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
The property specified by <i>key</i> is not an <b>IPortableDeviceKeyCollection</b> interface.

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



<a href="https://msdn.microsoft.com/f470cb89-e7a0-470d-83d1-eb643b062e45">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

