---
UID: NF:sensorsapi.ISensorEvents.OnDataUpdated
title: ISensorEvents::OnDataUpdated (sensorsapi.h)
description: Provides sensor event data.
helpviewer_keywords: ["ISensorEvents interface","OnDataUpdated method","ISensorEvents.OnDataUpdated","ISensorEvents::OnDataUpdated","OnDataUpdated","OnDataUpdated method","OnDataUpdated method","ISensorEvents interface","sensorsapi/ISensorEvents::OnDataUpdated","winsensors_com_ref.isensorevents_ondataupdated"]
old-location: winsensors_com_ref\isensorevents_ondataupdated.htm
tech.root: winsensors
ms.assetid: dda03a66-ffdb-4f1f-a6e4-17075eab7e00
ms.date: 12/05/2018
ms.keywords: ISensorEvents interface,OnDataUpdated method, ISensorEvents.OnDataUpdated, ISensorEvents::OnDataUpdated, OnDataUpdated, OnDataUpdated method, OnDataUpdated method,ISensorEvents interface, sensorsapi/ISensorEvents::OnDataUpdated, winsensors_com_ref.isensorevents_ondataupdated
f1_keywords:
- sensorsapi/ISensorEvents.OnDataUpdated
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
- ISensorEvents.OnDataUpdated
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorEvents::OnDataUpdated


## -description


Provides sensor event data.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface of the sensor that raised the event.


### -param pNewData [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a> interface that contains the event data.


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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a>
 

 

