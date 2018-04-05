---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetBufferValue
title: IPortableDeviceValues::SetBufferValue method
author: windows-driver-content
description: The SetBufferValue method adds a new BYTE* value (type VT_VECTOR | VT_UI1) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setbuffervalue.htm
old-project: wpd_sdk
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetBufferValue method, IPortableDeviceValues::SetBufferValue, IPortableDeviceValuesSetBufferValue, SetBufferValue method [Windows Portable Devices SDK], SetBufferValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetBufferValue,IPortableDeviceValues.SetBufferValue, portabledevicetypes/IPortableDeviceValues::SetBufferValue, wpdsdk.iportabledevicevalues_setbuffervalue
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
-	IPortableDeviceValues.SetBufferValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetBufferValue method


## -description



The <b>SetBufferValue</b> method adds a new <b>BYTE</b>* value (type VT_VECTOR | VT_UI1) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param pValue [in]

A <b>BYTE*</b> that contains the data to write to the item. The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.


### -param cbValue [in]

The size of the value pointed to by <i>pValue</i>, in bytes.


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



If an existing value has the same key that is specified by the <i>key</i> parameter, it overwrites the existing value without any warning. The existing key memory is released appropriately.

Setting a <b>NULL</b> or a zero-sized buffer is not supported.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/18180a47-7d81-440b-b596-2516089a02bd">IPortableDeviceValues::GetBufferValue</a>
 

 

