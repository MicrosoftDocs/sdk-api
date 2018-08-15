---
UID: NF:sbe.ISBE2GlobalEvent.GetEvent
title: ISBE2GlobalEvent::GetEvent
author: windows-sdk-content
description: Gets a global spanning event and its data from a Stream Buffer Source filter.
old-location: mstv\isbe2globalevent_getevent.htm
old-project: mstv
ms.assetid: 2ffa323d-6793-49e2-98ea-b9349c946c7c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEvent, GetEvent method [Microsoft TV Technologies], GetEvent method [Microsoft TV Technologies],ISBE2GlobalEvent interface, ISBE2GlobalEvent interface [Microsoft TV Technologies],GetEvent method, ISBE2GlobalEvent.GetEvent, ISBE2GlobalEvent::GetEvent, mstv.isbe2globalevent_getevent, sbe/ISBE2GlobalEvent::GetEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2GlobalEvent.GetEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

