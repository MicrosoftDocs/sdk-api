---
UID: NF:sensorsapi.ISensor.GetProperty
title: ISensor::GetProperty
author: windows-sdk-content
description: Retrieves a property value.
old-location: winsensors_com_ref\isensor_getproperty.htm
old-project: SensorsAPI
ms.assetid: 205f372e-a8ca-4494-a431-84d985ec4f9f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProperty, GetProperty method, GetProperty method,ISensor interface, ISensor interface,GetProperty method, ISensor.GetProperty, ISensor::GetProperty, sensorsapi/ISensor::GetProperty, winsensors_com_ref.isensor_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SensorConnectionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensor.GetProperty
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensor::GetProperty


## -description


Retrieves a property value.


## -parameters




### -param key [in]

<b>REFPROPERTYKEY</b> specifying the property value to be retrieved.


### -param pProperty [out]

<b>PROPVARIANT</b> pointer that receives the property value.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)
</b></dt>
</dl>
</td>
<td width="60%">
The sensor does not support the specified property. The value provided through <i>pProperty</i> is <b>VT_NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pProperty.

</td>
</tr>
</table>
 




## -remarks



To retrieve multiple property values as a collection, call <a href="https://msdn.microsoft.com/19581a45-500f-4210-9ec2-b3e33c84fb8a">ISensor::GetProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

