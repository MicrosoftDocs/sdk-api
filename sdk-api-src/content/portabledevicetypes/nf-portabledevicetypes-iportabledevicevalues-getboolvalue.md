---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetBoolValue
title: IPortableDeviceValues::GetBoolValue method
author: windows-driver-content
description: The GetBoolValue method retrieves a Boolean value (type VT_BOOL) specified by a key.
old-location: wpdsdk\iportabledevicevalues_getboolvalue.htm
old-project: wpd_sdk
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetBoolValue method [Windows Portable Devices SDK], GetBoolValue method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetBoolValue,IPortableDeviceValues.GetBoolValue, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetBoolValue method, IPortableDeviceValues::GetBoolValue, IPortableDeviceValuesGetBoolValue, portabledevicetypes/IPortableDeviceValues::GetBoolValue, wpdsdk.iportabledevicevalues_getboolvalue
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
-	IPortableDeviceValues.GetBoolValue
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetBoolValue method


## -description



The <b>GetBoolValue</b> method retrieves a <b>Boolean</b> value (type VT_BOOL) specified by a key.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> key that specifies the item to retrieve.


### -param pValue [out]

Pointer to the retrieved <b>BOOL</b> value.


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
The property specified by <i>key</i> is not a <b>BOOL</b> type.

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



<a href="https://msdn.microsoft.com/add30665-78f7-4037-801e-af51a4ab2f60">IPortableDeviceValues::SetBoolValue</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/1c003534-96b4-419b-94d1-73b5ffa2eba1">Setting Properties for a Single Object</a>



<a href="https://msdn.microsoft.com/f762a571-83ea-4999-ad49-a51044bc790d">Writing Content-Object Properties</a>
 

 

