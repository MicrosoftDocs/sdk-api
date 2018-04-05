---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetUnsignedIntegerValue
title: IPortableDeviceValues::SetUnsignedIntegerValue method
author: windows-driver-content
description: The SetUnsignedIntegerValue method adds a new ULONG value (type VT_UI4) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setunsignedintegervalue.htm
old-project: wpd_sdk
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetUnsignedIntegerValue method, IPortableDeviceValues::SetUnsignedIntegerValue, IPortableDeviceValuesSetUnsignedIntegerValue, SetUnsignedIntegerValue method [Windows Portable Devices SDK], SetUnsignedIntegerValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetUnsignedIntegerValue,IPortableDeviceValues.SetUnsignedIntegerValue, portabledevicetypes/IPortableDeviceValues::SetUnsignedIntegerValue, wpdsdk.iportabledevicevalues_setunsignedintegervalue
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
-	IPortableDeviceValues.SetUnsignedIntegerValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetUnsignedIntegerValue method


## -description



The <b>SetUnsignedIntegerValue</b> method adds a new <b>ULONG</b> value (type VT_UI4) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>ULONG</b> that specifies the new value.


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



If an existing value has the same key that is specified by the <i>key</i> parameter, it overwrites the existing value without any warning.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/275fda71-61ef-4b50-96fe-bdc0c0266646">Specifying Client Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/167163fa-6583-4e6b-b801-3a441a95644b">IPortableDeviceValues::GetUnsignedIntegerValue</a>



<a href="https://msdn.microsoft.com/275fda71-61ef-4b50-96fe-bdc0c0266646">Specifying Client Information</a>
 

 

