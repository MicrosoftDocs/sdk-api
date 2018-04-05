---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetStringValue
title: IPortableDeviceValues::SetStringValue method
author: windows-driver-content
description: The SetStringValue method adds a new string value (type VT_LPWSTR) or overwrites an existing one.
old-location: wpdsdk\iportabledevicevalues_setstringvalue.htm
old-project: wpd_sdk
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], SetStringValue method, IPortableDeviceValues::SetStringValue, IPortableDeviceValuesSetStringValue, SetStringValue method [Windows Portable Devices SDK], SetStringValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, SetStringValue,IPortableDeviceValues.SetStringValue, portabledevicetypes/IPortableDeviceValues::SetStringValue, wpdsdk.iportabledevicevalues_setstringvalue
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
-	IPortableDeviceValues.SetStringValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::SetStringValue method


## -description



The <b>SetStringValue</b> method adds a new string value (type VT_LPWSTR) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

A <b>LPCWSTR</b> that specifies the new value. The string is copied, so the caller can release the memory allocated for this value after calling this method.


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



Any existing key memory will be released appropriately.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/275fda71-61ef-4b50-96fe-bdc0c0266646">Specifying Client Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/c6feecc0-7a06-4f78-9cf1-e2897333b62e">IPortableDeviceValues::GetStringValue</a>



<a href="https://msdn.microsoft.com/0686ba54-4782-42a4-8fdb-2325fc8d8bc2">Setting Properties for Multiple Objects</a>



<a href="https://msdn.microsoft.com/1c003534-96b4-419b-94d1-73b5ffa2eba1">Setting Properties for a Single Object</a>



<a href="https://msdn.microsoft.com/275fda71-61ef-4b50-96fe-bdc0c0266646">Specifying Client Information</a>



<a href="https://msdn.microsoft.com/f762a571-83ea-4999-ad49-a51044bc790d">Writing Content-Object Properties</a>
 

 

