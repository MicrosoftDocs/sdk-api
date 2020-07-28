---
UID: NF:sensorsapi.ISensorCollection.GetAt
title: ISensorCollection::GetAt (sensorsapi.h)
description: Retrieves the sensor at the specified index in the collection.
helpviewer_keywords: ["GetAt","GetAt method","GetAt method","ISensorCollection interface","ISensorCollection interface","GetAt method","ISensorCollection.GetAt","ISensorCollection::GetAt","sensorsapi/ISensorCollection::GetAt","winsensors_com_ref.isensorcollection_getat"]
old-location: winsensors_com_ref\isensorcollection_getat.htm
tech.root: winsensors
ms.assetid: 3117a46d-62f2-4d69-97e1-1a75c08a799e
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method, GetAt method,ISensorCollection interface, ISensorCollection interface,GetAt method, ISensorCollection.GetAt, ISensorCollection::GetAt, sensorsapi/ISensorCollection::GetAt, winsensors_com_ref.isensorcollection_getat
f1_keywords:
- sensorsapi/ISensorCollection.GetAt
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
- ISensorCollection.GetAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorCollection::GetAt


## -description


Retrieves the sensor at the specified index in the collection.


## -parameters




### -param ulIndex [in]

<b>ULONG</b> containing the index of the sensor to retrieve.


### -param ppSensor [out]

Address of an <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> pointer that receives the pointer to the specified sensor.


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
NULL was passed in for ppSensor.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>
 

 

