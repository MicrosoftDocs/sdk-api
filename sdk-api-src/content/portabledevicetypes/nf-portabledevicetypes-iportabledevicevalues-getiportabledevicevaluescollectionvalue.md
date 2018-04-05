---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
title: IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method
author: windows-driver-content
description: The GetIPortableDeviceValuesCollectionValue method retrieves an IPortableDeviceValuesCollection value (type VT_UNKNOWN) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getiportabledevicevaluescollectionvalue.htm
old-project: wpd_sdk
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIPortableDeviceValuesCollectionValue method [Windows Portable Devices SDK], GetIPortableDeviceValuesCollectionValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetIPortableDeviceValuesCollectionValue,IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetIPortableDeviceValuesCollectionValue method, IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue, IPortableDeviceValuesGetIPortableDeviceValuesCollectionValue, portabledevicetypes/IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue, wpdsdk.iportabledevicevalues_getiportabledevicevaluescollectionvalue
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
-	IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method


## -description



The <b>GetIPortableDeviceValuesCollectionValue</b> method retrieves an <b>IPortableDeviceValuesCollection</b> value (type VT_UNKNOWN) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param ppValue [out]

Address of a variable that receives a pointer to the retrieved <a href="https://msdn.microsoft.com/library/windows/hardware/ff597598">IPortableDeviceValuesCollection</a> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.


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
The property specified by <i>key</i> is not an <b>IPortableDeviceValuesCollection</b> interface.

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



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff597633">SetIPortableDeviceValuesCollectionValue</a>
 

 

