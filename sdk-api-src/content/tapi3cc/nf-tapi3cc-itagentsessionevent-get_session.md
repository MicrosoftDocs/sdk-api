---
UID: NF:tapi3cc.ITAgentSessionEvent.get_Session
title: ITAgentSessionEvent::get_Session method
author: windows-driver-content
description: The get_Session method gets a pointer to the ITAgentSession on which the event occurred.
old-location: tapi3\itagentsessionevent_get_session.htm
old-project: Tapi
ms.assetid: 2868e5db-f596-424d-bd6a-0f0c5f52e1e7
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITAgentSessionEvent, ITAgentSessionEvent interface [TAPI 2.2], get_Session method, ITAgentSessionEvent::get_Session, _tapi3_itagentsessionevent_get_session, get_Session method [TAPI 2.2], get_Session method [TAPI 2.2], ITAgentSessionEvent interface, get_Session,ITAgentSessionEvent.get_Session, tapi3.itagentsessionevent_get_session, tapi3cc/ITAgentSessionEvent::get_Session
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3cc.h
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAgentSessionEvent.get_Session
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSessionEvent::get_Session method


## -description


The 
<b>get_Session</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> on which the event occurred.


## -parameters




### -param ppSession [out]

Pointer to the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppSession</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface returned by <b>ITAgentSessionEvent::get_Session</b>. The application must call <b>Release</b> on the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b">ITAgentSessionEvent</a>
 

 

