---
UID: NF:sensorsapi.ISensorCollection.RemoveByID
title: ISensorCollection::RemoveByID
author: windows-sdk-content
description: Removes a sensor from the collection. The sensor to be removed is specified by its ID.
old-location: winsensors_com_ref\isensorcollection_removebyid.htm
old-project: SensorsAPI
ms.assetid: 933ea072-d62c-4274-a2c0-69282ecb79d2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISensorCollection interface,RemoveByID method, ISensorCollection.RemoveByID, ISensorCollection::RemoveByID, RemoveByID, RemoveByID method, RemoveByID method,ISensorCollection interface, sensorsapi/ISensorCollection::RemoveByID, winsensors_com_ref.isensorcollection_removebyid
ms.prod: windows
ms.technology: windows-sdk
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
 - ISensorCollection.RemoveByID
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorCollection::RemoveByID


## -description


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




<a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a>
 

 

