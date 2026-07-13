---
UID: NF:sensorsapi.ISensorCollection.GetCount
title: ISensorCollection::GetCount (sensorsapi.h)
description: Retrieves the count of sensors in the collection.
helpviewer_keywords: ["GetCount","GetCount method","GetCount method","ISensorCollection interface","ISensorCollection interface","GetCount method","ISensorCollection.GetCount","ISensorCollection::GetCount","sensorsapi/ISensorCollection::GetCount","winsensors_com_ref.isensorcollection_getcount"]
old-location: winsensors_com_ref\isensorcollection_getcount.htm
tech.root: winsensors
ms.assetid: 40bcf993-55fb-4d75-91dc-44d770a0e226
ms.date: 09/19/2025
ms.keywords: GetCount, GetCount method, GetCount method,ISensorCollection interface, ISensorCollection interface,GetCount method, ISensorCollection.GetCount, ISensorCollection::GetCount, sensorsapi/ISensorCollection::GetCount, winsensors_com_ref.isensorcollection_getcount
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
 - ISensorCollection::GetCount
 - sensorsapi/ISensorCollection::GetCount
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
 - ISensorCollection.GetCount
---

# ISensorCollection::GetCount


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the count of sensors in the collection.

## -parameters

### -param pCount [out]

Address of a <b>ULONG</b> that receives the count.

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
NULL was passed in for pCount.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>