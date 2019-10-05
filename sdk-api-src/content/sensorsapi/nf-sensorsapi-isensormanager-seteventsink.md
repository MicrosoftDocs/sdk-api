---
UID: NF:sensorsapi.ISensorManager.SetEventSink
title: ISensorManager::SetEventSink (sensorsapi.h)
author: windows-sdk-content
description: Specifies the interface through which to receive sensor manager event notifications.
old-location: winsensors_com_ref\isensormanager_seteventsink.htm
tech.root: SensorsAPI
ms.assetid: 270f0943-dc6a-47df-b1bd-ecfbfcafc4c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISensorManager interface,SetEventSink method, ISensorManager.SetEventSink, ISensorManager::SetEventSink, SetEventSink, SetEventSink method, SetEventSink method,ISensorManager interface, sensorsapi/ISensorManager::SetEventSink, winsensors_com_ref.isensormanager_seteventsink
ms.topic: method
f1_keywords: 
 - "sensorsapi/ISensorManager.SetEventSink"
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
 - ISensorManager.SetEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorManager::SetEventSink


## -description


Specifies the interface through which to receive sensor manager event notifications.


## -parameters




### -param pEvents [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents">ISensorManagerEvents</a> callback interface that receives the event notifications. Set to <b>NULL</b> to stop receiving event notifications.


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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>
 

 

