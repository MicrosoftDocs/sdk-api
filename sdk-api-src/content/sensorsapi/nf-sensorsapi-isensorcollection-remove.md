---
UID: NF:sensorsapi.ISensorCollection.Remove
title: ISensorCollection::Remove (sensorsapi.h)
description: Removes a sensor from the collection. The sensor is specified by a pointer to the ISensor interface to be removed.
helpviewer_keywords: ["ISensorCollection interface","Remove method","ISensorCollection.Remove","ISensorCollection::Remove","Remove","Remove method","Remove method","ISensorCollection interface","sensorsapi/ISensorCollection::Remove","winsensors_com_ref.isensorcollection_remove"]
old-location: winsensors_com_ref\isensorcollection_remove.htm
tech.root: winsensors
ms.assetid: 9e96bae1-9ac8-41fd-99c7-3c025baf674a
ms.date: 09/19/2025
ms.keywords: ISensorCollection interface,Remove method, ISensorCollection.Remove, ISensorCollection::Remove, Remove, Remove method, Remove method,ISensorCollection interface, sensorsapi/ISensorCollection::Remove, winsensors_com_ref.isensorcollection_remove
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
 - ISensorCollection::Remove
 - sensorsapi/ISensorCollection::Remove
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
 - ISensorCollection.Remove
---

# ISensorCollection::Remove


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Removes a sensor from the collection. The sensor is specified by a pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface to be removed.

## -parameters

### -param pSensor [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface to remove from the collection.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified sensor is not part of the collection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>