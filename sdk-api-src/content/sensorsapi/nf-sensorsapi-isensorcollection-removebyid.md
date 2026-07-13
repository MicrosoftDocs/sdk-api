---
UID: NF:sensorsapi.ISensorCollection.RemoveByID
title: ISensorCollection::RemoveByID (sensorsapi.h)
description: Removes a sensor from the collection. The sensor to be removed is specified by its ID.
helpviewer_keywords: ["ISensorCollection interface","RemoveByID method","ISensorCollection.RemoveByID","ISensorCollection::RemoveByID","RemoveByID","RemoveByID method","RemoveByID method","ISensorCollection interface","sensorsapi/ISensorCollection::RemoveByID","winsensors_com_ref.isensorcollection_removebyid"]
old-location: winsensors_com_ref\isensorcollection_removebyid.htm
tech.root: winsensors
ms.assetid: 933ea072-d62c-4274-a2c0-69282ecb79d2
ms.date: 09/19/2025
ms.keywords: ISensorCollection interface,RemoveByID method, ISensorCollection.RemoveByID, ISensorCollection::RemoveByID, RemoveByID, RemoveByID method, RemoveByID method,ISensorCollection interface, sensorsapi/ISensorCollection::RemoveByID, winsensors_com_ref.isensorcollection_removebyid
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
 - ISensorCollection::RemoveByID
 - sensorsapi/ISensorCollection::RemoveByID
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
 - ISensorCollection.RemoveByID
---

# ISensorCollection::RemoveByID


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Removes a sensor from the collection. The sensor to be removed is specified by its ID.

## -parameters

### -param sensorID [in]

The <b>GUID</b> of the sensor to remove from the collection.

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