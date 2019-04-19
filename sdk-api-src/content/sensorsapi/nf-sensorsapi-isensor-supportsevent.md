---
UID: NF:sensorsapi.ISensor.SupportsEvent
title: ISensor::SupportsEvent (sensorsapi.h)
author: windows-sdk-content
description: Indicates whether the sensor supports the specified event.
old-location: winsensors_com_ref\isensor_supportsevent.htm
tech.root: SensorsAPI
ms.assetid: abf4e339-651d-4444-b219-e5177dbaa7ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISensor interface,SupportsEvent method, ISensor.SupportsEvent, ISensor::SupportsEvent, SupportsEvent, SupportsEvent method, SupportsEvent method,ISensor interface, sensorsapi/ISensor::SupportsEvent, winsensors_com_ref.isensor_supportsevent
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
 - ISensor.SupportsEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensor::SupportsEvent


## -description


Indicates whether the sensor supports the specified event.


## -parameters




### -param eventGuid [in]

<b>REFGUID</b> value specifying the event to search for.


### -param pIsSupported [out]

Address of a <b>VARIANT_BOOL</b> that receives a value indicating whether the sensor supports the event.


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
NULL was passed in for pIsSupported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

