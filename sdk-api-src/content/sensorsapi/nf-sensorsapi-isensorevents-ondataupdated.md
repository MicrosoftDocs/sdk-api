---
UID: NF:sensorsapi.ISensorEvents.OnDataUpdated
title: ISensorEvents::OnDataUpdated
author: windows-sdk-content
description: Provides sensor event data.
old-location: winsensors_com_ref\isensorevents_ondataupdated.htm
tech.root: SensorsAPI
ms.assetid: dda03a66-ffdb-4f1f-a6e4-17075eab7e00
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISensorEvents interface,OnDataUpdated method, ISensorEvents.OnDataUpdated, ISensorEvents::OnDataUpdated, OnDataUpdated, OnDataUpdated method, OnDataUpdated method,ISensorEvents interface, sensorsapi/ISensorEvents::OnDataUpdated, winsensors_com_ref.isensorevents_ondataupdated
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISensorEvents.OnDataUpdated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sensorsapi.h
: 
- ISensorEvents.OnDataUpdated
: 
---

# ISensorEvents::OnDataUpdated


## -description


Provides sensor event data.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface of the sensor that raised the event.


### -param pNewData [in]

Pointer to the <a href="https://msdn.microsoft.com/c677b956-e3ab-477c-b97b-aceec4e2d235">ISensorDataReport</a> interface that contains the event data.


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
 




## -see-also




<a href="https://msdn.microsoft.com/41acbb4f-b4f8-4573-a993-ed93ec9494f0">ISensorEvents</a>
 

 

