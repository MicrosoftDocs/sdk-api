---
UID: NF:sensorsapi.ISensorCollection.Remove
title: ISensorCollection::Remove
author: windows-sdk-content
description: Removes a sensor from the collection. The sensor is specified by a pointer to the ISensor interface to be removed.
old-location: winsensors_com_ref\isensorcollection_remove.htm
old-project: SensorsAPI
ms.assetid: 9e96bae1-9ac8-41fd-99c7-3c025baf674a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISensorCollection interface,Remove method, ISensorCollection.Remove, ISensorCollection::Remove, Remove, Remove method, Remove method,ISensorCollection interface, sensorsapi/ISensorCollection::Remove, winsensors_com_ref.isensorcollection_remove
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
 - ISensorCollection.Remove
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorCollection::Remove


## -description


Removes a sensor from the collection. The sensor is specified by a pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface to be removed.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface to remove from the collection.


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
 

 

