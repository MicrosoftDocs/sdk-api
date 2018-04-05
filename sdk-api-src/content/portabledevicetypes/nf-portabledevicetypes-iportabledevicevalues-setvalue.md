---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetValue
title: IPortableDeviceValues::SetValue method
author: windows-driver-content
description: The SetValue method adds a new PROPVARIANT value or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setvalue.htm
old-project: wpd_sdk
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetValue method, IPortableDeviceValues::SetValue, IPortableDeviceValuesSetValue, SetValue method [Windows Portable Devices SDK], SetValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetValue,IPortableDeviceValues.SetValue, portabledevicetypes/IPortableDeviceValues::SetValue, wpdsdk.iportabledevicevalues_setvalue
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
-	IPortableDeviceValues.SetValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetValue method


## -description



The <b>SetValue</b> method adds a new <b>PROPVARIANT</b> value or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param pValue [in]

A <b>PROPVARIANT</b> that specifies the new value. The SDK copies the value, so the caller can release the local variable by calling <b>PropVariantClear</b> after calling this method.


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
</table>
 




## -remarks



When the VARTYPE for <i>pValue</i> is VT_VECTOR or VT_UI1, setting a <b>NULL</b> or zero-sized buffer is not supported. For example, neither pValue.caub.pElems = <b>NULL</b> nor pValue.caub.cElems = 0 are allowed.



This method can be used to retrieve a value of any type from the collection. However, if you know the value type in advance, use one of the specialized <b>Set...</b> methods of this interface to avoid the overhead of working with PROPVARIANT values directly.

If an existing value has the same key that is specified by the <i>key</i> parameter, it overwrites the existing value without any warning. The existing key memory is released appropriately.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/927844f5-8f57-4596-ae0d-c67b8011ca87">IPortableDeviceValues::GetValue</a>



<a href="https://msdn.microsoft.com/864c23ee-5a4e-4e06-add0-f6aef5562430">IPortableDeviceValues::RemoveValue</a>
 

 

