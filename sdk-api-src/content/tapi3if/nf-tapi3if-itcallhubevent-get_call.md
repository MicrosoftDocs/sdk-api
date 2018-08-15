---
UID: NF:tapi3if.ITCallHubEvent.get_Call
title: ITCallHubEvent::get_Call
author: windows-sdk-content
description: The get_Call method returns a pointer to the ITCallInfo interface of the call on which the event occurred.
old-location: tapi3\itcallhubevent_get_call.htm
old-project: tapi
ms.assetid: 2ac47da3-f60f-41f4-99f7-031744044bd4
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallHubEvent interface [TAPI 2.2],get_Call method, ITCallHubEvent.get_Call, ITCallHubEvent::get_Call, _tapi3_itcallhubevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallHubEvent interface, tapi3.itcallhubevent_get_call, tapi3if/ITCallHubEvent::get_Call
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallHubEvent.get_Call
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallHubEvent::get_Call


## -description


The 
<b>get_Call</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface of the call on which the event occurred.


## -parameters




### -param ppCall [out]

<b>ITCallInfo</b> interface.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCallt</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



This method may return a <b>NULL</b> if the event is not associated with a call.




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/4008fc7e-f095-442d-9214-61bfead8cf04">ITCallHubEvent</a>
 

 

