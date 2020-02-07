---
UID: NF:sensorsapi.ISensor.GetSupportedDataFields
title: ISensor::GetSupportedDataFields (sensorsapi.h)
description: Retrieves a set of PROPERTYKEYs that represent the data fields the sensor can provide.
old-location: winsensors_com_ref\isensor_getsupporteddatafields.htm
tech.root: SensorsAPI
ms.assetid: b808e472-8428-4176-a3a1-2ab6e454ef44
ms.date: 12/05/2018
ms.keywords: GetSupportedDataFields, GetSupportedDataFields method, GetSupportedDataFields method,ISensor interface, ISensor interface,GetSupportedDataFields method, ISensor.GetSupportedDataFields, ISensor::GetSupportedDataFields, sensorsapi/ISensor::GetSupportedDataFields, winsensors_com_ref.isensor_getsupporteddatafields
f1_keywords:
- sensorsapi/ISensor.GetSupportedDataFields
dev_langs:
- c++
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
- ISensor.GetSupportedDataFields
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensor::GetSupportedDataFields


## -description


Retrieves a set of <b>PROPERTYKEY</b>s that represent the data fields the sensor can provide.


## -parameters




### -param ppDataFields [out]

Address of the <a href="https://go.microsoft.com/fwlink/p/?linkid=134661">IPortableDeviceKeyCollection</a>  pointer that receives the list of supported data fields.


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
NULL was passed in for ppDataFields.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>
 

 

