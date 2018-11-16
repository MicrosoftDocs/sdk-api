---
UID: NF:sensorsapi.ISensor.SetProperties
title: ISensor::SetProperties
author: windows-sdk-content
description: Specifies sensor properties.
old-location: winsensors_com_ref\isensor_setproperties.htm
tech.root: SensorsAPI
ms.assetid: f2bed074-fcee-4dbb-a4c1-d5922d65d3b9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISensor interface,SetProperties method, ISensor.SetProperties, ISensor::SetProperties, SetProperties, SetProperties method, SetProperties method,ISensor interface, sensorsapi/ISensor::SetProperties, winsensors_com_ref.isensor_setproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
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
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensor.SetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sensorsapi.h
: 
- ISensor.SetProperties
: 
---

# ISensor::SetProperties


## -description


Specifies sensor properties.


## -parameters




### -param pProperties [in]

 Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> interface containing the list of properties and values to set.


### -param ppResults [out]

Address of an <b>IPortableDeviceValues</b> interface that receives the list of properties that were successfully set. Each property has an associated <b>HRESULT</b> value, which indicates whether setting the property succeeded.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The request to set one or more of the specified properties failed. Inspect <i>ppResults</i> to determine which properties, if any, succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppResults.

</td>
</tr>
</table>
 




## -remarks



This method enables you to specify the values of one or more  properties, such as the sensor make, model, and serial number, by making a single call. 

Not all properties can be set.

<b>IPortableDeviceValues</b> is defined by the Windows Portable Devices API.


#### Examples

For an example of how to set properties, see <a href="https://msdn.microsoft.com/7d10e5b4-bae7-4564-84eb-75c6a2eeef8f">Setting and Retrieving Sensor Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/19581a45-500f-4210-9ec2-b3e33c84fb8a">GetProperties</a>



<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

