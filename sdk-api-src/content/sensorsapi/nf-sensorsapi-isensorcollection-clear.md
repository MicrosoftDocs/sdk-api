---
UID: NF:sensorsapi.ISensorCollection.Clear
title: ISensorCollection::Clear
author: windows-sdk-content
description: Empties the sensor collection.
old-location: winsensors_com_ref\isensorcollection_clear.htm
old-project: SensorsAPI
ms.assetid: 03b2345b-1d06-449e-9ecf-ecce9aa60c08
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Clear, Clear method, Clear method,ISensorCollection interface, ISensorCollection interface,Clear method, ISensorCollection.Clear, ISensorCollection::Clear, sensorsapi/ISensorCollection::Clear, winsensors_com_ref.isensorcollection_clear
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
 - ISensorCollection.Clear
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorCollection::Clear


## -description


Empties the sensor collection.


## -parameters






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




<a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a>
 

 

