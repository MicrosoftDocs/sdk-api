---
UID: NF:sensorsapi.ISensor.GetEventInterest
title: ISensor::GetEventInterest (sensorsapi.h)
description: Retrieves the current event interest settings.
helpviewer_keywords: ["GetEventInterest","GetEventInterest method","GetEventInterest method","ISensor interface","ISensor interface","GetEventInterest method","ISensor.GetEventInterest","ISensor::GetEventInterest","sensorsapi/ISensor::GetEventInterest","winsensors_com_ref.isensor_geteventinterest"]
old-location: winsensors_com_ref\isensor_geteventinterest.htm
tech.root: winsensors
ms.assetid: 8324817e-c310-4b90-b5b4-c7e113e3502e
ms.date: 09/19/2025
ms.keywords: GetEventInterest, GetEventInterest method, GetEventInterest method,ISensor interface, ISensor interface,GetEventInterest method, ISensor.GetEventInterest, ISensor::GetEventInterest, sensorsapi/ISensor::GetEventInterest, winsensors_com_ref.isensor_geteventinterest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensor::GetEventInterest
 - sensorsapi/ISensor::GetEventInterest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensor.GetEventInterest
---

# ISensor::GetEventInterest


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

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

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest">SetEventInterest</a>