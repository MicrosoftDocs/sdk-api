---
UID: NF:sensorsapi.ISensorCollection.Clear
title: ISensorCollection::Clear (sensorsapi.h)
description: Empties the sensor collection.
helpviewer_keywords: ["Clear","Clear method","Clear method","ISensorCollection interface","ISensorCollection interface","Clear method","ISensorCollection.Clear","ISensorCollection::Clear","sensorsapi/ISensorCollection::Clear","winsensors_com_ref.isensorcollection_clear"]
old-location: winsensors_com_ref\isensorcollection_clear.htm
tech.root: winsensors
ms.assetid: 03b2345b-1d06-449e-9ecf-ecce9aa60c08
ms.date: 09/19/2025
ms.keywords: Clear, Clear method, Clear method,ISensorCollection interface, ISensorCollection interface,Clear method, ISensorCollection.Clear, ISensorCollection::Clear, sensorsapi/ISensorCollection::Clear, winsensors_com_ref.isensorcollection_clear
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
 - ISensorCollection::Clear
 - sensorsapi/ISensorCollection::Clear
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
 - ISensorCollection.Clear
---

# ISensorCollection::Clear


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Empties the sensor collection.



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
</table>

## -remarks

This method calls <b>Release</b> on all sensor interface pointers in the collection and frees any memory used by the collection.

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>
