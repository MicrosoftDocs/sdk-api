---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
title: IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method
author: windows-driver-content
description: The SetIPortableDeviceValuesCollectionValue method adds a new IPortableDeviceValuesCollection value (type VT_UNKNOWN) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setiportabledevicevaluescollectionvalue.htm
old-project: wpd_sdk
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetIPortableDeviceValuesCollectionValue method, IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue, IPortableDeviceValuesSetIPortableDeviceValuesCollectionValue, SetIPortableDeviceValuesCollectionValue method [Windows Portable Devices SDK], SetIPortableDeviceValuesCollectionValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetIPortableDeviceValuesCollectionValue,IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue, portabledevicetypes/IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue, wpdsdk.iportabledevicevalues_setiportabledevicevaluescollectionvalue
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
-	IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method


## -description



The <b>SetIPortableDeviceValuesCollectionValue</b> method adds a new <b>IPortableDeviceValuesCollection</b> value (type VT_UNKNOWN) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param pValue [in]

Pointer to an <b>IPortableDeviceValuesCollection</b> interface that specifies the new value. The SDK copies a reference to the submitted interface and calls <b>AddRef</b> on it.


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




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/07b41ef8-d299-4d69-98ad-f1818c09ef6c">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue</a>
 

 

