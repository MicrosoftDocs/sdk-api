---
UID: NF:sensorsapi.ISensor.GetProperties
title: ISensor::GetProperties
author: windows-sdk-content
description: Retrieves multiple sensor properties.
old-location: winsensors_com_ref\isensor_getproperties.htm
tech.root: SensorsAPI
ms.assetid: 19581a45-500f-4210-9ec2-b3e33c84fb8a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetProperties, GetProperties method, GetProperties method,ISensor interface, ISensor interface,GetProperties method, ISensor.GetProperties, ISensor::GetProperties, sensorsapi/ISensor::GetProperties, winsensors_com_ref.isensor_getproperties
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
 - ISensor.GetProperties
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
- ISensor.GetProperties
: 
---

# ISensor::GetProperties


## -description


Retrieves multiple sensor properties.


## -parameters




### -param pKeys [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=134661">IPortableDeviceKeyCollection</a> interface containing the <b>PROPERTYKEY</b> collection for the property values being requested. Set to <b>NULL</b> to retrieve all supported properties.


### -param ppProperties [out]

Address of an <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> pointer that receives the pointer to the requested property values.


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
The sensor driver does not support at least one of the specified properties. Each unsupported property <b>PROPVARIANT</b> returned through the <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> interface will have its error value set to <b>HRESULT_FROM_WIN32 
(ERROR_NOT_FOUND)</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppProperties.

</td>
</tr>
</table>
 




## -remarks



This method enables you to retrieve the values of multiple properties, such as the sensor make, model, and serial number, by making a single call. To retrieve a single property, call <a href="https://msdn.microsoft.com/205f372e-a8ca-4494-a431-84d985ec4f9f">ISensor::GetProperty</a>.

The <b>IPortableDeviceKeyCollection</b> and <b>IPortableDeviceValues</b> interfaces are defined by the Windows Portable Devices API. 


#### Examples

For an example of how to retrieve properties from a sensor,  see <a href="https://msdn.microsoft.com/7d10e5b4-bae7-4564-84eb-75c6a2eeef8f">Setting and Retrieving Sensor Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/2fb739a0-9af5-4784-94b2-f8d10b9e21ca">Sensor Properties</a>



<a href="https://msdn.microsoft.com/f2bed074-fcee-4dbb-a4c1-d5922d65d3b9">SetProperties</a>
 

 

