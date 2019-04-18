---
UID: NF:tapi3if.ITCallStateEvent.get_Cause
title: ITCallStateEvent::get_Cause (tapi3if.h)
author: windows-sdk-content
description: The get_Cause method gets the cause associated with this event.
old-location: tapi3\itcallstateevent_get_cause.htm
tech.root: Tapi
ms.assetid: e3a4b985-1c0f-4e93-a965-c61c9c0ab10d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent interface [TAPI 2.2],get_Cause method, ITCallStateEvent.get_Cause, ITCallStateEvent::get_Cause, _tapi3_itcallstateevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITCallStateEvent interface, tapi3.itcallstateevent_get_cause, tapi3if/ITCallStateEvent::get_Cause
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallStateEvent.get_Cause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallStateEvent::get_Cause


## -description


The 
<b>get_Cause</b> method gets the cause associated with this event.


## -parameters




### -param pCEC [out]

Pointer to 
<a href="https://msdn.microsoft.com/9bc9e050-41f7-4330-a263-db745d3fa3f8">CALL_STATE_EVENT_CAUSE</a> indicator.


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
The <i>pCEC</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9bc9e050-41f7-4330-a263-db745d3fa3f8">CALL_STATE_EVENT_CAUSE</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/0885ef81-726d-41ca-be8c-b3ff2e02fc3c">ITCallStateEvent</a>
 

 

