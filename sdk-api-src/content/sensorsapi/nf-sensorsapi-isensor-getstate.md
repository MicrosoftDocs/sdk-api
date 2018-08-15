---
UID: NF:sensorsapi.ISensor.GetState
title: ISensor::GetState
author: windows-sdk-content
description: Retrieves the current operational state of the sensor.
old-location: winsensors_com_ref\isensor_getstate.htm
old-project: SensorsAPI
ms.assetid: ec8683a5-f2b3-48ce-8732-16429ee16a7f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetState, GetState method, GetState method,ISensor interface, ISensor interface,GetState method, ISensor.GetState, ISensor::GetState, sensorsapi/ISensor::GetState, winsensors_com_ref.isensor_getstate
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
 - ISensor.GetState
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensor::GetState


## -description


Retrieves the current operational state of the sensor.


## -parameters




### -param pState [out]

Address of a <a href="https://msdn.microsoft.com/4cf993ba-d767-4ef8-94a9-e819cc210360">SensorState</a> variable that receives the current state.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver did not provide a state value. The value provided through <i>pState</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pState.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

