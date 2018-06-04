---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISBE2GlobalEvent::GetEvent


## -description


Gets a global spanning event and its data from a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter. 


## -parameters




### -param idEvt [in]

GUID identifying the event.


### -param param1 [in]

First event-specific parameter.


### -param param2 [in]

Second event-specific parameter.


### -param param3 [in]

Third  event-specific parameter.


### -param param4 [in]

Fourth  event-specific parameter.


### -param pSpanning [out]

Receives a flag indicating whether the event is a spanning event.


### -param pcb [in, out]

Pointer to a value specifying the buffer size. If the <i>pb</i> parameter is <b>NULL</b>, this parameter returns the required buffer size.


### -param pb [out]

Pointer to a buffer that receives the event data. If this parameter is <b>NULL</b>, the <i>pcb</i> parameter returns the required buffer size. The structure of the event data depends on the event type. For a list of event types, see the description of the <a href="https://msdn.microsoft.com/f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef">ISBE2SpanningEvent::GetEvent</a> method.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INSUFFICIENT_BUFFER</dt>
</dl>
</td>
<td width="60%">
Buffer was too small to hold event data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_CONTEXT_EXPIRED</dt>
</dl>
</td>
<td width="60%">
Too much time elapsed between the broadcast event and the call to retrieve it.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/18bb9f8a-df97-468c-acb2-be7fa61a4789">ISBE2GlobalEvent</a>



<a href="https://msdn.microsoft.com/f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef">ISBE2SpanningEvent::GetEvent</a>



<a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source Filter</a>
 

 

