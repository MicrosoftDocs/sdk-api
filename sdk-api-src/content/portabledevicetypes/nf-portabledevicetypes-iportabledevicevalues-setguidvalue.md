---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetGuidValue
title: IPortableDeviceValues::SetGuidValue method
author: windows-driver-content
description: The SetGuidValue method adds a new GUID value (type VT_CLSID) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setguidvalue.htm
old-project: wpd_sdk
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetGuidValue method, IPortableDeviceValues::SetGuidValue, IPortableDeviceValuesSetGuidValue, SetGuidValue method [Windows Portable Devices SDK], SetGuidValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetGuidValue,IPortableDeviceValues.SetGuidValue, portabledevicetypes/IPortableDeviceValues::SetGuidValue, wpdsdk.iportabledevicevalues_setguidvalue
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
-	IPortableDeviceValues.SetGuidValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetGuidValue method


## -description



The <b>SetGuidValue</b> method adds a new <b>GUID</b> value (type VT_CLSID) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>REFGUID</b> that contains the new value.


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




## -see-also




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/1cfa75e8-2c3b-4893-954e-dae25a6b8220">IPortableDeviceValues::GetGuidValue</a>
 

 

