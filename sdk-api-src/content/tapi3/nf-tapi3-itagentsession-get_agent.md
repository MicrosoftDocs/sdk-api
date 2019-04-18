---
UID: NF:tapi3.ITAgentSession.get_Agent
title: ITAgentSession::get_Agent (tapi3.h)
author: windows-sdk-content
description: The get_Agent method gets a pointer to the ITAgent interface associated with this session.
old-location: tapi3\itagentsession_get_agent.htm
tech.root: Tapi
ms.assetid: 1378f7f1-020e-492c-8f1a-f4e8a9c7c3e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_Agent method, ITAgentSession.get_Agent, ITAgentSession::get_Agent, _tapi3_itagentsession_get_agent, get_Agent, get_Agent method [TAPI 2.2], get_Agent method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_agent, tapi3cc/ITAgentSession::get_Agent
ms.topic: method
req.header: tapi3.h
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
 - ITAgentSession.get_Agent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentSession::get_Agent


## -description


The 
<b>get_Agent</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> interface associated with this session.


## -parameters




### -param ppAgent [out]

pointer to 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> interface.


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
The <i>ppAgent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> interface returned by <b>ITAgentSession::get_Agent</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>
 

 

