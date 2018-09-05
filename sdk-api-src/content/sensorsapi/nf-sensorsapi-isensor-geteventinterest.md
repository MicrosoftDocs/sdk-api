---
UID: NF:sensorsapi.ISensor.GetEventInterest
title: ISensor::GetEventInterest
author: windows-sdk-content
description: Retrieves the current event interest settings.
old-location: winsensors_com_ref\isensor_geteventinterest.htm
old-project: SensorsAPI
ms.assetid: 8324817e-c310-4b90-b5b4-c7e113e3502e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetEventInterest, GetEventInterest method, GetEventInterest method,ISensor interface, ISensor interface,GetEventInterest method, ISensor.GetEventInterest, ISensor::GetEventInterest, sensorsapi/ISensor::GetEventInterest, winsensors_com_ref.isensor_geteventinterest
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
 - ISensor.GetEventInterest
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensor::GetEventInterest


## -description


Retrieves the current event interest settings.


## -parameters




### -param ppValues [out]

Address of a <b>GUID</b> pointer that points to an array of sensor event identifiers.


### -param pCount [out]

The count of <b>GUID</b>s in the array pointed to by <i>ppValues</i>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppValues or pCount.

</td>
</tr>
</table>
 




## -remarks



Each sensor event is represented by a <b>GUID</b>. This method returns the list of requested events as an array of <b>GUID</b>s.




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/d3c2d8b9-6511-41ff-9734-92f47825bbcd">SetEventInterest</a>
 

 

