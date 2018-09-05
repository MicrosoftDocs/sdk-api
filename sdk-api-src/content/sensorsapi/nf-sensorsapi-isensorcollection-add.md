---
UID: NF:sensorsapi.ISensorCollection.Add
title: ISensorCollection::Add
author: windows-sdk-content
description: Adds a sensor to the collection.
old-location: winsensors_com_ref\isensorcollection_add.htm
old-project: SensorsAPI
ms.assetid: 7f563d5d-2943-4cbd-bfb5-c347ec270e85
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Add, Add method, Add method,ISensorCollection interface, ISensorCollection interface,Add method, ISensorCollection.Add, ISensorCollection::Add, sensorsapi/ISensorCollection::Add, winsensors_com_ref.isensorcollection_add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
req.redist: 
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
 - ISensorCollection.Add
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorCollection::Add


## -description


Adds a sensor to the collection.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface for the sensor to add to the collection.


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




<a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a>
 

 

