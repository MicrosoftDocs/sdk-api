---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetKeyValue
title: IPortableDeviceValues::SetKeyValue method
author: windows-driver-content
description: The SetKeyValue method adds a new REFPROPERTYKEY value (type VT_UNKNOWN) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setkeyvalue.htm
old-project: wpd_sdk
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetKeyValue method, IPortableDeviceValues::SetKeyValue, IPortableDeviceValuesSetKeyValue, SetKeyValue method [Windows Portable Devices SDK], SetKeyValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetKeyValue,IPortableDeviceValues.SetKeyValue, portabledevicetypes/IPortableDeviceValues::SetKeyValue, wpdsdk.iportabledevicevalues_setkeyvalue
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
-	IPortableDeviceValues.SetKeyValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetKeyValue method


## -description



The <b>SetKeyValue</b> method adds a new <b>REFPROPERTYKEY</b> value (type VT_UNKNOWN) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>REFPROPERTYKEY</b> that specifies the new value.


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




## -see-also




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/2c92b1c0-3ea6-4a14-8b63-d57752b649b8">IPortableDeviceValues::GetKeyValue</a>
 

 

