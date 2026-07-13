---
UID: NF:sensorsapi.ISensorCollection.Add
title: ISensorCollection::Add (sensorsapi.h)
description: Adds a sensor to the collection.
helpviewer_keywords: ["Add","Add method","Add method","ISensorCollection interface","ISensorCollection interface","Add method","ISensorCollection.Add","ISensorCollection::Add","sensorsapi/ISensorCollection::Add","winsensors_com_ref.isensorcollection_add"]
old-location: winsensors_com_ref\isensorcollection_add.htm
tech.root: winsensors
ms.assetid: 7f563d5d-2943-4cbd-bfb5-c347ec270e85
ms.date: 09/19/2025
ms.keywords: Add, Add method, Add method,ISensorCollection interface, ISensorCollection interface,Add method, ISensorCollection.Add, ISensorCollection::Add, sensorsapi/ISensorCollection::Add, winsensors_com_ref.isensorcollection_add
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
 - ISensorCollection::Add
 - sensorsapi/ISensorCollection::Add
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
 - ISensorCollection.Add
---

# ISensorCollection::Add


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Adds a sensor to the collection.

## -parameters

### -param pSensor [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface for the sensor to add to the collection.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)
</b></dt>
</dl>
</td>
<td width="60%">
The sensor collection already contains a sensor with the specified ID.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>