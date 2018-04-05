---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetValue
title: IPortableDeviceValues::GetValue method
author: windows-driver-content
description: The GetValue method retrieves a PROPVARIANT value specified by a key.
old-location: wpdsdk\iportabledevicevalues_getvalue.htm
old-project: wpd_sdk
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetValue method [Windows Portable Devices SDK], GetValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetValue,IPortableDeviceValues.GetValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetValue method, IPortableDeviceValues::GetValue, IPortableDeviceValuesGetValue, portabledevicetypes/IPortableDeviceValues::GetValue, wpdsdk.iportabledevicevalues_getvalue
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
-	IPortableDeviceValues.GetValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetValue method


## -description



The <b>GetValue</b> method retrieves a <b>PROPVARIANT</b> value specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>PROPVARIANT</b> value. The caller must release the memory by calling <b>PropVariantClear</b> when done with it.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The property specified by <i>key</i> is not in the collection.

</td>
</tr>
</table>
 




## -remarks



When the VARTYPE for <i>pValue</i> is VT_VECTOR or VT_UI1, retrieving a <b>NULL</b> or zero-sized buffer is not supported. For example, neither pValue.caub.pElems = <b>NULL</b> nor pValue.caub.cElems = 0 are allowed.



This method can be used to retrieve a value of any type from the collection. However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/864c23ee-5a4e-4e06-add0-f6aef5562430">IPortableDeviceValues::RemoveValue</a>



<a href="https://msdn.microsoft.com/69630a21-79e9-4c96-8ed7-9a41ebb991cd">IPortableDeviceValues::SetValue</a>
 

 

